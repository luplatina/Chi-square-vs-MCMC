# Chi2-vs-MCMC
Compare and evaluate the practicability of Chi-square and MCMC in curves fitting

##OVERVIEW
Regression algorithem has been widely used in curves fitting projects.
Fitting parameters usually are obtained by minimizing the [cost fucntion (Chi-square function)](https://en.wikipedia.org/wiki/Goodness_of_fit).
Markov Chain Monte Carlo (MCMC) is a typical Algorithem in Bayesian Statistics. The prediction of fitting parameters can be modeled as  building a Bayesian model for the fitting parameters, and solving by MCMC method. This code is the demostration to show the advantages and
concerned points, when implementing these two method in curves fitting.

##EXPLANTATION

Advantages of Chi-square fitting are as follows:
1. Chi-square fitting allows the uncertainty of observed y value to get involved in to the cost function as the weighting factors. 
2. The uncertainty of fitting variables can be obtained by caculating the covariance matrix, corresponding to Chi-square dependence on the fitting parameters.
In practice, approciate evalutation of the uncertainty on observed y is important for the error bar evaluation of fitting parameters. And a hidden hypothesis is that the error bar on observed y assume the stochastic of observed y is Gaussian ditribution. Such rigid hypothesis may not be practical or easy to justified for some complicated problems.

In my opinion, MCMC considers the curves fitting process as the probablity prediction(posterior) of fitting parameter based on the observed y probablity(prior) and the fit model(likelihood). MCMC may take some time to reach the final equilibrium distribution of the posterior, but its random walking strategies can avoid the local minimium problem in Chi-square fitting, and its prior probabity is a more flexible hyprothesis for the uncertainty of observed y than Chi-square fitting. Therefore, MCMC could have more pratical value when dealing complicated, high dimensional problems.
