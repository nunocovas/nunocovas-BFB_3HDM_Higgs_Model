# nunocovas-BFB_3HDM_Higgs_Model
This repository contains a code that implements a global optimization routine, to check the vacuum stability condition known as Boundedness From Bellow (BFB) in the 3HDM, a multiple Higgs doublet model of Particle Physics.

The assumptions of the potential are written in the file 3HDM_potential.pdf

The code assumes that a txt file with 45 columns is provided as input, with each column representing one of the 45 degrees of freedom (9 real couplings + 18 complex couplings) of the general 3HDM. The complex couplings require 2 consecutive columns for the real and imaginary components. The code always assumes the general 3HDM, therefore, to consider a more restrictive model, with different symmetries, the unnecessary couplings must be set at 0 in the input file.

The code is released as a jupyter notebook (version 5.4.6), that runs on the Anaconda navigator. 
The navigator can be installed in the command line, following the process presented in the webpage: [https://anaconda.org/anaconda/python](url) 
The code was developed using the numpy and scipy packages; the numba package is used for performance and the parallelization depends on the joblib package, therefore all of these should be installed before running the notebook. If the numba or joblib packages are not installed by default, both can be easily downloaded using the following links: [https://anaconda.org/numba/numba](url) and [https://anaconda.org/anaconda/joblib](url)

After verifying the installation of all relevant packages, launch the Anaconda navigator and the jupyter notebook application. Download the file BFB.ipynb and open it with jutyter notebook. Change the name of the input file in the first cell of the notebook, to match the name of the input file in your directory. Click on the "run all cells" option to run the code. 

The input file must have more than 1 set of couplings, otherwise, the code will not function.

The user can adjust the numerical tolerance and number of restarts. A lower numerical tolerance or a greater number of restarts ensures a better determination of the minimum, at the cost of more computation time.  
A tolerance of 1e-4 or less and at least 5 restarts is advised.

The output of the code is a txt file with the couplings, plus an additional column with a boolean flag: 0 if the set of couplings is BFB and 1 otherwise.
