# Generalized linear models

The term <font color='orange'>generalized</font> refers to specifying different observational models from the exponential family, denoted by $F$, for the observations $y$. The models are linked to a predictor function $\eta$ by a specific <font color='orange'>link function</font> $g(·)$,

$$
p(y|\eta, \phi) = F (y|\mu, \phi),\\
g(\mu) = \eta,
$$

where $\mu$ represents the mean of the model, $E[y | \phi] = \mu$, and $\phi$ represents the other parameters of the model, such as, for example, the variance parameter in normal models or the shape parameter in Gamma models. 

The predictor function $\eta$, often also called <font color='orange'>linear predictor</font>, is usually linked to the mean parameter $\mu$ of the model (although it might also be another parameter of the model) by a strictly monotonic link function $g$ with inverse mapping 

$$
\mu = g^{−1}(\eta). 
$$

Often, $g$ is a differentiable function in order to be able to obtain the maximum likelihood estimate conveniently.

The term <font color='orange'>linear model</font> usually refers to using a parametric form for the functional relationship (predictor function $\eta$) between observed data and predictors (input variables), such that:

$$
\eta = \beta x,
$$

```{margin}
You might be more familiar with the terms 'feature' or 'independent variables' or 'covariate' other than 'predictor'. We will be using them interchangeably.
```
where $\beta$ is the row-vector of coefficients in a parametric model and $x$ is the column vector of predictors.

In the Bayesian framework, we will need to provide prior distributions for the model parameters $\mu$ and $\phi$. In the case of the mean parameter $\mu$, if we have a predictor function, we will define the priors in the parameters $\beta$ instead.

## Normal model

The observational model is a Normal distribution with parameters mean $\mu$ and noise variance $\sigma^2$:

$$
\begin{align*}
p(y|\mu, \sigma) &= \mathcal{N} (y|\mu, \sigma^2),\\
\mu &= \eta.
\end{align*}
$$

In this case, the canonical link function is the identity function.

We have seen an example of such model in the "Bayesian workflow" section. Remember computing `mu = b0 + b1 * weight` there?

## Poisson model

The observations in this case are non-negative integer values. They are expected to follow a Poisson distribution with mean parameter $\mu$:

$$
\begin{align*}
p(y|\lambda) &= \mathcal{\text{Pois}} (y|\lambda),\\
\log(\lambda) &=\eta
\end{align*}
$$

In this case, the link function is the log-function allowing to transform the values of the linear predictor $\eta$ in the continuous real space, to the strictly positive or equal to zero range of values of the mean of the Poisson model $\lambda = \exp(\eta)$.

## Binomial model

In this case, the observations are binary $y \in (0,1)$. These binary observations are expected to follow a Binomial distribution, with probability parameter $p$:

$$
\begin{align*}
p(y|\eta) &= \mathcal{\text{Binom}} (p),\\
\text{logit}(p) &= \eta.
\end{align*}
$$

In this case, the probability $p$ is linked to the predictor function $\eta$ through the ’logistic’ transformation, $\text{logit}(·)$, which transforms the values of the predictor function, usually in the continuous real space, to the [0,1] range of probabilities. In this model, the ’probit’ link function can also be used. 


## Categorical model
```{margin}
Categorical model is also called "multinomial".
```

In multi-class classification problems, the observations are multi-class-valued $(1, . . . , J )$. In this case, a multinomial observational model may be used:

$$
\begin{align*}
p(y | p) &= \mathcal{\text{Categorical}}(p),\\
p &= \text{softmax}(\eta)
\end{align*}
$$

where $p = (p_1,...,p_j,...,p_J)$ is a vector of probabilities of each possible class. In this model, in order the vector of probabilities $p$ of an observation to sum to 1, $\sum_{j=1}^J p_j = 1$.

The probability of belonging to a class $j$ can be computed by the ’softmax’ transformation

$$
p_j = \frac{\exp(\eta_j)}{\sum_{k=1}^J \exp(\eta_k)}.
$$