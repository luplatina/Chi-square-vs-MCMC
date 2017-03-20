# Chi2-vs-MCMC
Compare and evaluate the practicability of Chi-square and MCMC in curves fitting

## OVERVIEW
Regression algorithm has been widely used in curves fitting projects.
Fitting parameters usually are obtained by minimizing the [cost fucntion (Chi-square function)](https://en.wikipedia.org/wiki/Goodness_of_fit).
Markov Chain Monte Carlo (MCMC) is a typical Algorithm in Bayesian Statistics. The prediction of fitting parameters can be modeled as  building a Bayesian model for the fitting parameters, and solving by MCMC method. This code is the demonstration to show the advantages and
concerned points, when implementing these two method in curves fitting.

## DISCUSSION

Advantages of Chi-square fitting are as follows:

1. Chi-square fitting allows the uncertainty of observed y value to get involved in to the cost function as the weighting factors. 

2. The uncertainty of fitting variables can be obtained by calculating the covariance matrix, corresponding to Chi-square dependence on the fitting parameters.

In practice, appropriate evaluation of the uncertainty on observed y is important for the error bar evaluation of fitting parameters. And a hidden hypothesis is that the error bar on observed y assumes the stochastic of observed y is Gaussian distribution. Such rigid hypothesis may not be practical or easy to justify for the cases with poor understanding on data variance.

In my opinion, MCMC considers the curves fitting process as the probability prediction(posterior) of fitting parameter based on the observed y probability(prior) and the fit model(likelihood). The model optimization process is handeled by Gibbs sampling algorithm. MCMC may take some time to reach the final equilibrium distribution of the posterior, but its random walking strategies can avoid the local minimum problem in Chi-square fitting, and its prior probabity is a more flexible hypothesis for the uncertainty of observed y than Chi-square fitting. Therefore, MCMC could have more practical value when dealing complicated, high dimensional problems.
