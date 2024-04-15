# nunocovas-BFB_3HDM_Higgs_Model
This repository contains a code that checks the vacuum stability conditions known as Boundedness From Bellow, BFB, in the 3HDM, a multiple Higgs model of Particle Physics.

The assumptions of the potential are writen in the file 3HDM_potential.pdf

The code assumes that a txt file with 45 collumns is provided as input, with each column representing one of the 45 degrees of freedom (9 real lambdas + 18 complex lambdas) of the general 3HDM. To consider a more restrictive model, keep the unnecessary columns at 0.

The code was produced using jupyter notebook version 5.4.6, from the anaconda distribuction. 
The code was developed using the numpy and scipy packages, the numba package is used for performance and the paralelization depends on the joblib package, therefore these packages should be installed before running the notebook.

The user can adjust the numerical tolerance and number of restarts. It is advised to use a tolerance of 1e-4 or less and at least 5 restarts.

The output of this code is a txt file with all sets of couplings that the code considers BFB.
