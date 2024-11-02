# nunocovas-BFB_3HDM_Higgs_Model
This repository contains a code that implements a global optimization routine, to check the vacuum stability condition known as Boundedness From Bellow (BFB) in the 3HDM, a multiple Higgs doublet model of Particle Physics.

The assumptions of the potential are written in the file 3HDM_potential.pdf

The code assumes that a txt file with 45 columns is provided as input, with each column representing one of the 45 degrees of freedom (9 real lambdas + 18 complex lambdas) of the general 3HDM. To consider a more restrictive model, keep the unnecessary columns at 0.

The code was produced using jupyter notebook version 5.4.6, from the Anaconda distribution. 
The code was developed using the numpy and scipy packages, the numba package is used for performance and the paralelization depends on the joblib package, therefore these packages should be installed before running the notebook.

The user can adjust the numerical tolerance and number of restarts. Using a tolerance of 1e-4 or less and at least 5 restarts is advised.

The output of this code is a txt file with all sets of couplings that the code considers BFB.
