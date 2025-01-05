---
title: Setup
---

# Run exercises in cmslpc

Open a terminal/console, connect to cmslpc-sl7 and prepare your working area:

~~~
kinit yourlpcusername@FNAL.GOV
ssh -Y yourlpcusername@cmslpc-sl7.fnal.gov
~~~
{: .language-bash}

If you haven't done it yet, go to your `nobackup` area (`/uscms_data/d3/<YOUR USERNAME>/`) and create a folder for the CMSDAS exercises. Once you are there you can setup CMSSW and clone our repository:

~~~
cd ~/nobackup
mkdir METDAS
cd METDAS

source /cvmfs/cms.cern.ch/cmsset_default.sh
cmsrel CMSSW_12_4_11_patch3
cd CMSSW_12_4_11_patch3/src
cmsenv

git clone git@github.com:garvitaa/METDAS.git -b DASJan2025
scram b -j4
~~~
{: .language-bash}

> ## Remember
> Once you clone the repository, using the `DASJan2025` branch, the necessary are located
> in `METDAS/MET_Analysis/test`
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
