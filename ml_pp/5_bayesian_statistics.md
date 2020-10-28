# 5 Bayesian statistics

## 5.1 Introduction

MAP - maximum a posteriori: parameter estimates O_hat = argmax p(Thetha|D)
p(Theta|D) - posterior
p(x|D) - posterior predictive density

Bayesian statistics core idea: use posterior distribution to sum up all we know about a set of unkown variables.
Bayesian interpretation of probability: probability to quantify uncertainty about something (information).


## 5.2 Summarizing posterior distributions

What quantities can be derived from the posterior p(Theta|D)? In this section we discuss such summary statistics as MAP estimation, credible intervals, and inference for a difference in proportions.

### MAP estimation

We can compute point estimate of an unkown quantity by computing the posterior mean, median, or mode.
Posterior mode (aka MAP estimate) is often used because:
- it can be represented as an optimization problem, hence, good algorithms exist for it
- can be interpreted in non-bayesian terms (log prior of the regularizer)
However, ther are also some drawbacks:
- no measure of uncertainty (credible intervals are here to help!)
- plugging in the MAP estimates can lead to overconfidence, overfitting
- the mode is often a poor choice as a summary. What to do then? Decision theory! Specify a loss function F(Theta, Theta_hat)


### Credible intervals

A contiguous region C = (l,u) which contains 1 - alpha of the posterior probability mass.
Do not confuse with confidence intervals from frequentists statistics!


### Inference for a difference in proportions

Sometimes we have multiple input parameters and we want to compute the posterior distribution using these parameters. For example consider [this Amazon sellsers comparison case](https://www.johndcook.com/blog/2011/09/27/bayesian-amazon/).

## 5.3 Bayesian model selection

Model selection problem: how to choose the best model among the set of models (family of parametric distributions) of different complexity?

K-CV vs Bayesian model selection: K-fold cross-validation is less unefficient as it requires to fit a model K times. Bayesian model selection, on the other hand allows to compute posterior over models p(m|D), what boils down to computing p(D|m) (aka marginal likelihood, integrated likelihood, or the evidence of model m).

### Bayesian Occam's razor
Models with more parameters do not neccessarily have higher marginal likelihood.
Conservation probability mass principle: complex models, which can predict many things, must spread their probability mass thinly. Hence, they will not obtain as large probability for any given data set as simpler models.

### Computing the marignal likelihood (evidence) p(D|m)

Easy to compute with conjugate priors.

Can be also approximated with Bayesian information criterion (BIC)

### Bayes factors

Ratio of marginal likelihoods of two models (cf. p-values)

## Priors

Bayesian statistics relies on priors, i.e., certain assumptions about the world. There are some techniques to minimize impact of the priors

### Uninformative prior
Let the data speak for itself!

The right uninformative prior: Beta(1/2, 1/2).

Important: always perform a sensitivity analysis to check how priors, likelihoods, and data preprocessing influence model behaviour. Good model should be non-sensitive to those.

### Robust priors

Robust priors have heavy tails which avoids forcing things to be too close to the prior mean. Drawback: can be computationally expensive.

### Conjugate priors

Less robust than robust priors but also less computationally expensive.


## 5.5 Hierarchical Bayes

Putting prior on priors.

## 5.6 Empirical Bayes

Computationally cheap approximation to inference in a hierarchical Bayesian model.

## 5.7 Bayesian decision theory

How to turn our updated beliefs about the world into actions.



