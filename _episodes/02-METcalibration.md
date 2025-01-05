---
title: "MET Calibrations"
teaching: 20
exercises: 10
questions:
- "Why do we need to calibrate MET? How is the performance measured?"
- "What are the different ways of calibrating MET at CMS?"
- "What is MET-$\phi$ modulation? How to correct for it?"
objectives:
- "Learn about the MET calibration procedure and techniques used at CMS."
- "Learn about measuring MET performance."
- "Understand MET-$\phi$ modulation and how to account for it."
keypoints:
- "Inaccurate MET estimation can arise from sources such as nonlinearity in the calorimeter's response to hadrons, minimum energy thresholds in the calorimeters, and pT thresholds or inefficiencies in track reconstruction, and is mitigated through calibration procedures described in this exercise."
- "Type-1 MET is the default MET calibration recommended in CMS."
- "Type-1 smear MET improves the data-MC agreement, and JME POG recommends analysts to evaluate its impact in your studies."
---

## MET Corrections

$$\vec{p}_{T}^{miss,~raw} = - \sum_{i \in all} \vec{p}_{T, i} $$

The MET objects described earlier (PF-MET and PUPPI-MET) are referred to as _raw_ MET, and they are systematically different from the _true_ MET, which corresponds to the transverse momentum carried by invisible particles.
This difference arises from factors such as the non-compensating nature of the calorimeters, calorimeter thresholds, and detector misalignment, among others.
To improve the MET estimate and make it closer to the true MET, corrections can be applied. 


### Type-1 Correction

The **Type-I correction** is the most commonly used MET correction in CMS.
It propagates the jet energy corrections (JEC) to MET. Specifically, the Type-I correction replaces the vector sum of the transverse momenta of particles clustered as jets with the vector sum of the transverse momenta of the jets, which have been corrected with JEC.

Particles can be classified into two disjoint sets: those that are clustered as jets and those that remain unclustered.

$$\vec{p}_{T}^{miss,~raw} = - \sum_{i \in jets} \vec{p}_{T, i} - \sum_{i \in uncl} \vec{p}_{T, i}$$

The first vector sum corresponds to the total pT of all jets:

$$\sum_{i \in jets} \vec{p}_{T, i} = \sum_{i}^{nJets} \vec{p}_{T, jet}^{uncorr}$$

The superscript "uncorr" indicates that the jet energy correction (JEC) has not yet been applied to these jets.

The Type-I correction replaces the raw jet pT with the corrected jet pT. The Type-I correction can be expressed as the difference between two vector sums:

$$C_{T}^{Type-1} = \sum_{i}^{nJets} \vec{p}_{T, jet}^{uncorr} - \sum_{i}^{nJets} \vec{p}_{T, jet}^{corr}$$

or equivalently:

$$C_{T}^{Type-1} = \sum_{i \in jets} \vec{p}_{T, i} - \sum_{i}^{nJets} \vec{p}_{T, jet}^{corr}$$

This vector term can be added to the raw MET to obtain the Type-1 corrected MET:

$$\vec{p}_{T}^{miss,~Type-1} = \vec{p}_{T}^{miss,~raw} + C_{T}^{Type-1}$$

Thus, the Type-I corrected MET is:

$$\vec{p}_{T}^{miss,~Type-1} = \vec{p}_{T}^{miss,~raw} - \sum_{i}^{nJets} (\vec{p}_{T, jet}^{corr} - \vec{p}_{T, jet}^{uncorr}) $$


$$\vec{p}_{T}^{miss,~Type-1} = - \sum_{i}^{nJets} \vec{p}_{T, jet}^{corr} - \sum_{i \in uncl} \vec{p}_{T, i}$$

> ## Remember
> PF MET is the recommended MET algorithm in Run~2, and PUPPI MET is recommended for Run~3 analyses.
> Type-I corrected MET is the default MET calibration required in all analyses.
{: .callout}

### Type-1 Smear MET (For MC Only)

In MC simulations, jets are smeared to achieve better agreement with data. This smearing of _MC jets_ can additionally be propagated to MET, resulting in **Type-1 smear MET**.

### XY corrections
The XY correction reduces the MET $\phi$ modulation. This correction also helps mitigate pile-up effects.

The distribution of true MET is independent of $\phi$ due to the rotational symmetry of collisions around the beam axis.
However, we observe that the reconstructed MET does depend on $\phi$.
The MET $\phi$ distribution follows roughly a sinusoidal curve with a period of $2\pi$.

The possible causes of this modulation include:
- Anisotropic detector responses
- Inactive calorimeter cells
- Detector misalignment
- Displacement of the beam spot

The amplitude of the modulation increases roughly linearly with the number of pile-up interactions.

## MET performance
A well-measured Z boson or photon provides a unique event axis and a precise momentum scale for evaluating MET performance.
To achieve this, the response and resolution of MET are studied in samples where a Z boson decays to a pair of electrons or muons, or in events with an isolated photon.
**Such events should have little to no genuine MET.**
The MET performance is then assessed by comparing the momentum of the vector boson to that of the hadronic recoil system.
The hadronic recoil system is defined as the vector sum of the transverse momenta of all PF candidates, excluding the vector boson (or its decay products in the case of Z boson decay).


{% include links.md %}
