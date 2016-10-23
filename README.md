# Chi2-vs-MCMC
Compare and evaluate the practicability of Chi-square and MCMC in curves fitting
Regression algorithem has been widely used in curves fitting projects.
Fitting variables usually are obtained by minimizing the cost fucntion (Chi-square function). 
some advantages comparing to other regression algorithem are as follows:
1. Chi-square fitting allows the uncertainty of observed y value to get involved in to the cost function as the weighting factors. 
2. The uncertainty of fitting variables can be obtained by caculating the Chi-square dependence on the fitting variables.
In practice, I notice that approciate evalutation of error bar on observed y is important for the error bar evalutation of fitting 
variables. And a hiden hypothesis is that the error bar on observed y assume the stochastic of observed y is Gaussian ditribution.
I feel that is a very rigid hypothesis
Recently, I notice that MCMC method can deal the rigid hythothesis in a more fexible way, which make it a practical method for some 
undefined or underdevelop data situtations.
