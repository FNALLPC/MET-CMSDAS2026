---
layout: lesson
root: .  # Is the only page that doesn't follow the pattern /:path/index.html
permalink: index.html  # Is the only page that doesn't follow the pattern /:path/index.html
---

<img src="fig/met_schematic.png" alt="" style="width: 400px;"/>

This tutorial will give you the basics you need to deal with missing transverse energy (MET) in your analysis. We start with an introduction to MET reconstruction and the fundamental concepts underlying its calculation, ensuring a solid foundation for understanding its role in physics analyses. Next, we delve into MET calibration and uncertainties, providing the tools to accurately account for and quantify potential deviations. Finally, we cover the identification of sources that can lead to artificial MET and discuss Noisy Event filters (formerly known as MET filters) designed to mitigate such effects, equipping you to confidently handle MET-related challenges in your research.

The tutorial is designed to be executed at cmslpc, following the setup step, using jupyter notebooks. On this website, you will find links to instructional slides and more information about the topics to walk you through the exercises.

_For general questions, problems, debugs, or asking for help from experts on jet and MET:_ [CMS Talk JetMET category](https://cms-talk.web.cern.ch/c/pog/jetmet/51)

_Follow the CMS workbook on MET analysis:_ [WorkBookMETAnalysis](https://twiki.cern.ch/twiki/bin/view/CMSPublic/WorkBookMetAnalysis)

> ## What is this set of exercises trying to do?
>
>It gives you hands-on experience accessing the MET collection in an event, plotting basic quantities, and applying MET corrections.
> * This is a 101 guide to accessing MET in the CMS framework without assuming prior knowledge of MET analysis.
> * It aims to make you familiar with basic MET types and how to use them in your analysis.
> * Each exercise is illustrated using real-life example scripts.
> * It provides a comprehensive reference to more advanced workbook examples, additional resources, and pedagogical documentation in one place.
{: .objectives}

> ## What are these exercises NOT meant for?
>
> To provide a comprehensive summary of the CMS JetMET software machinery for MET analyses performed at CMS.
{: .keypoints}

> ## What do we expect from you?
>
> * You should have completed all the pre-exercises and have a CMS LPC account, a valid grid certificate, and access to a current web browser.
> * It is essential that you work through the notebooks, ensuring you understand each step and every plot.
> * The exercises are designed to be run directly on CMSLPC, with scripts provided for you to follow and discuss the exercises.
{: .testimonial}

### Facilitators CMSDAS LPC 2025

<img src="fig/photo_facilitators.jpeg" alt="" style="width:80%">


### Support

Join the [ShortExMET Mattermost channel](https://mattermost.web.cern.ch/cmsdaslpc2025/channels/shortexmet) and don't hesitate to ask for help from the facilitators in the room.


<!-- this is an html comment -->
{% comment %} This is a comment in Liquid {% endcomment %}

> ## Prerequisites
> - [CMS DAS Pre-exercises](https://fnallpc.github.io/cms-das-pre-exercises/)
> - [Jets and Pileup short excercise](https://cms-jet.github.io/JMEDAS/) 
{: .prereq}

{% include links.md %}
