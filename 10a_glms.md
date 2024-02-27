# Generalized linear models

The term *generalized* refers to specifying different observational models from the exponential family, denoted by $F$ , for the observations $y$. The models are linked to a predictor function $\eta$ by a specific *link function* $g(·)$,

$$
p(y|\eta, \phi) = F (y|\mu, \phi),\\
g(\mu) = \eta,
$$
where $\mu$ represents the mean of the model, $E[y|\phi] = \mu$, and $\phi$ represent the other parameters of the model, such as, for example, the variance parameter in normal models or the shape parameter in gamma models. 

The predictor function $\eta$, often also called <font color='orange'>linear predictor</font>, is usually linked to the mean parameter μ of the model (although it might also be another parameter of the model) by a strictly monotonic link function $g$ with inverse mapping 

$$
\mu = g^{−1}(\eta). 
$$

Often, $g$ is a differentiable function in order to be able to obtain the maximum likelihood estimate conveniently.

The term *linear model* usually refers to using a parametric form for the functional relationship (predictor function η) between observed data and predictors (input variables), such that:

$$
\eta = \beta x,
$$

where $\beta$ is the row-vector of coefficients in a parametric model and x is the column vector of input values (in this work, the terms input variable, covariate and predictor are used interchangeably). In parametric models the form of predictor functions are defined by a finite, often small, set of parameters $\beta$. Parametric models fit possible nonlinear effects through, for example, binning or polynomials.
In the Bayesian framework, prior distributions have to be defined for the model parameters $\mu$ and $\phi$. In the case of the mean parameter $\mu$, if we have a predictor function, we will define the priors in the parameters $\beta$ of the predictor function instead.

## Normal model

The observational model is a Normal distribution with parameters mean $\mu$ and noise variance $\sigma^2$:

$$
p(y|\mu, \sigma) = \mathcal{N} (y|\mu, \sigma^2),\\
\mu = \eta.
$$

In this case, the canonical link function is the identity function.

## Poisson model

The observations are expected to follow a Poisson distribution with mean parameter $\mu$:

$$
p(y|\mu) = \mathcal{\text{Pois}} (y|\mu),\\
\log(\mu) =\eta
$$

In this case, the link function is, for example, the log function, in order to transform the values of the predictor function $\eta$, usually in the continuous real space, to the strictly positive or equal to zero range of values of the mean of the Poisson model.

## Binomial model

In this case, the observations are binary-valued $(0,1)$ observations. These binary observations are expected to follow a Binomial distribution, with probability parameter $p$ of being 1:

$$
p(y|\mu) = \mathcal{\text{Binom}} (p),\\
\text{logit}(p) = \eta.
$$

In this case, the probability $p$ is linked to the predictor function η through the ’logistic’ transformation, logit(·), which transforms the values of the predictor function, usually in the continuous real space, to the [0,1] range of probabilities.

In this model, the ’probit’ link function can also be used. 

## Multinomial model

In multi-class classification problems, the observations are multi-class-valued $(1, . . . , J )$. In this case, a multinomial observational model may be used:

$$
p(y) = \mathcal{\text{Multinom}}(p),
$$

where $p = (p_1,...,p_j,...,p_J)$ is a vector of probabilities of each possible class. In this model, in order the vector of probabilities $p$ of an observation to sum to 1, $\sum_{j=1}^J p_j = 1$.

The probability of belonging to a class $j$ can be computed by the ’softmax’ transformation

$$
p_j = \frac{\exp(\eta_j)}{\sum_{k=1}^J \exp(\eta_k)}.
$$