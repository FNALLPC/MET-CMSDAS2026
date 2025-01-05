---
title: "High anomalous MET in events and it's treatment"
teaching: 20
exercises: 10
questions:
- "What is anomalous MET?"
- "How to identify these events?"
objectives:
- "Learn about anomalous MET"
- "Learn about the Noisy event filters and their implementation."
keypoints:
- "Jet substructure is the field study the internakl structure of high pt jets, usually clustered with a bigger jet radius (AK8)."
- "Grooming algorithms like softdrop, and substructure variables like the nsubjettiness ratio help us to identify the origin of these jets."
- "Over the years more state-of-the-art taggers involving ML have been implemented in CMS. Those help us indentify more effectively boosted jets."
---

> ## After following the instructions in the setup:
>
> ~~~
> FIXME
> ~~~
> {: .language-bash}
>
> This will open a jupyter notebook tree with various notebooks. 
{: .callout}

## What is anomalous MET? 

Anomalous MET refers to situations where the measured MET in a particle collision event deviates from what is expected due to various factors, such as reconstruction failures, detector malfunctions, or background noise.
These anomalous MET events can arise from:
- **Detector Issues:** Malfunctions or mismeasurements in detectors, such as the electromagnetic calorimeter (ECAL) or hadronic calorimeter (HCAL), leading to spurious energy deposits.
- **Reconstruction Failures:** Errors in reconstructing particle tracks or energy, including issues with jets, leptons, or unclustered energy, that result in inaccurate MET calculations.
- **Non-collision Origins:** Spurious signals from sources unrelated to the particle collision, such as beam-halo particles, cosmic rays, or other environmental factors.
- **Dead or Malfunctioning Detector Cells:** Areas of the detector that fail to register energy deposits correctly, leading to underestimation of the MET.

In such events, the MET value may be much higher than expected and does not reflect true missing energy from invisible particles (like neutrinos or dark matter candidates).

## Noisy event filters

To identify false MET, several algorithms have been developed that analyze factors such as timing, pulse shape, and signal topology.
When fake MET is detected, the corresponding events are typically discarded.
These cleaning algorithms, or filters, run in separate processing paths, and the outcome (success or failure) is recorded as a filter decision bit.
Analyzers can use this decision bit to filter out noisy events. These filters are specifically designed to reject events with unusually large MET values caused by spurious signals.

{% include links.md %}

