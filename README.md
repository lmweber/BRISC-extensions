# BRISC-extensions

====

## Overview
Bootstrap for Rapid Inference on Spatial Covariances: Provides parameter estimates and bootstrap based confidence intervals for all parameters in a Gaussian Process based spatial regression model.


## Installation
In order to download the package, please run the following command in R:

```{r }
if (!require("devtools")) install.packages("devtools")
devtools::install_github("ArkajyotiSaha/BRISC-extensions")
```

## What's new?

* Evaluation of Log-likelihood with the MLE of the model parameters, available in `BRISC_estimation` as `log_likelihood` in the output. 
* Bypassing the ordering. The ordering was available as an output earlier in `BRISC_estimation`, but there was no way to bypass it. Now, in `BRISC_estimation`, the ordering can be bypassed by giving it as an input in `ordering`. 
* A code for ordering the coordinates, `BRISC_order`. Inputs are coordinates, ordering methods and verbose e.g. `BRISC_order(coords, order = "Sum_coords", verbose = TRUE)`. Output is the ordering of the coords and can be used as input for `ordering` in `Brisc_estimation`.
* Bypassing the neighbor selection and associated calculation (e.g. distance calculation, proper form of input for NNGP). The neighbor selection was available as an output earlier in `BRISC_estimation`, but there was no way to bypass it. Now, in `BRISC_estimation`, the neighbor selection can be bypassed by giving it as an input in `neighbor`. The input of `neighbor` has to be an output from `BRISC_neighbor`. Inputs of this code are coordinates, ordering methods and verbose e.g. `BRISC_neighbor(coords, order = "Sum_coords", verbose = TRUE)`.
* For convenience the ordering of the outputs in object `Brisc_out` was slightly altered, should not pose a major problem for users as there is no direct user interaction with this output. 
