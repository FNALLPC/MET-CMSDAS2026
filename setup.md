---
title: Setup
---

# Run exercises in cmslpc

Open a terminal/console, connect to cmslpc-el9 and prepare your working area:

~~~
kinit yourlpcusername@FNAL.GOV
ssh -Y yourlpcusername@cmslpc-el9.fnal.gov
~~~
{: .language-bash}

If you haven't done it yet, go to your `nobackup` area (`/uscms_data/d3/<YOUR USERNAME>/`) and create a folder for the CMSDAS exercises.

~~~
cd ~/nobackup
mkdir METDAS
cd METDAS
~~~
{: .language-bash}

Once you are there you can setup CMSSW and clone our repository:

~~~
source /cvmfs/cms.cern.ch/cmsset_default.sh
cmsrel CMSSW_14_0_7
cd CMSSW_14_0_7/src
cmsenv

git clone git@github.com:garvitaa/METDAS.git -b main
scram b -j4
~~~
{: .language-bash}

> ## Remember
> Once you clone the repository, using the `main` branch, the necessary scripts for this lesson are located in `METDAS/CMSDAS_MET_Analysis/test` and `METDAS/scripts`.
{: .callout}

Activate your grid certificate:
~~~
voms-proxy-init -voms cms -valid 192:00
~~~
{: .language-bash}

## Useful settings

If you like seeing your working directory in the commandline, you can do also this by adding a line to ~/.bashrc and activating it with the 'source' command:

~~~
echo "PS1='\W\$ '" >> ~/.bashrc
source ~/.bashrc
~~~
{: .language-bash}



{% include links.md %}
