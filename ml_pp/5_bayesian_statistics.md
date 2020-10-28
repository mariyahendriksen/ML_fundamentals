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

We can compute point estimate of an unkown quantity by computing the posterior mean, meadian, or mode.
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

## Bayesian model selection

## Priors

## Hierarchical Bayes

## Empirical Bayes

## Bayesian decision theory
