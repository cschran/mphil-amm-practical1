# MPhil in Scientific Computing - University of Cambridge
## Atomistic Materials Modelling Course - Practical 1


### Introduction
This practical is in ```01_MD-Fundamentals``` will let you work on a bare-bones MD code, and implement some of the key functions in order to run an MD simulation.

There is a solution notebook available for the pracitcal in the respective folder. However we _strongly_ reccommend that you do not look at these until after the practical or if you are desparately stuck. It is better to ask one of the demonstrators and talk through any problems than simply copying an answer (you might come up with a more efficient solutions!). 


#### Before you start

We will run this practical on one of the cerberus clusters that you have access to.
All software required for the completion has been installed there.

Adapt the following ssh command to your needs, please distribute over the three available clusters:\
`ssh -X USER@cerberus1/2/3.lsc.phy.private.cam.ac.uk`

For the rest of the practical work within a directory under `/data/cerberus1/2/3`. For example, if you logged into cerberus2, create a directory under your username:\
`mkdir /data/cerberus2/$USER`

Change to this directory and clone the github repository of this practical:\
`git clone https://github.com/cschran/mphil-amm-practical1.git`

Once you are in the directory, execute the following command to setup the correct system environment:\
`source setup.sh`


### Part 1: MD-Fundamentals

### MD Simulation of Liquid Argon

![Liquid argon simulation](https://github.com/cschran/mphil-amm-practical1/blob/main/01_MD-Fundamentals/argon.jpg)

In this section we will follow in the footsteps of Aneesur Rahman, who ran the first molecular dynamics computer simulation on liquid argon 60 years ago in 1964 [[1]](#1). Fittingly for this summer school, we will also be modelling the interactions between the Ar atoms with a Lennard Jones potential. 

```cd 01_MD-Fundamentals```

We have provided you with a skeleton of a molecular dynamics code in the ```MD.ipynb``` notebook.
Juptyer notebook is a web application for creating and sharing computational documents.
It offers a simple, streamlined, document-centric experience and has become a standard tool in the field to perform quick analysis and write code.

You can start a notebook on cerberus and then access it on your local machine.
In the main directory of the repository, execute `juptyer-notebook --no-browser`. This will lock up this session, so it is best to do it in a new terminal (remember to always source the setup.sh script if you open a new session!).

On your local machine, you can then use ssh to tunnel into the running session (replace XXXX to match the network address shown the by jupyter notebook):\
`ssh -N -y -L localhost:XXXX:localhost:XXXX USER@cerberus1/2/3.lsc.phy.private.cam.ac.uk`

Copying the shown network address into your local browser will allow you to access the session:\
`http://localhost:8888/?token=8d186032bbbe095b294789e863b065a546fcc15b68683c99`

Work through the notebook, filling in the required code to run an MD simulation of liquid Argon.


## References
<a id="1">[1]</a> 
A. Rahman
Phys. Rev. 136, A405 – Published 19 October 1964

## Acknowlegements
Many of the algorithms here have been inspired by those in:

Frenkel and Smit: Understanding Molecular Simulations: From Algorithms to Applications.
