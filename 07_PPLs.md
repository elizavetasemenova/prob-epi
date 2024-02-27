# Probabilistic Programming

## What is probabilistics programming

[Probabilistic programming](https://en.wikipedia.org/wiki/Probabilistic_programming) (PP) is a paradigm in computer programming that enables the creation of models and algorithms capable of <font color='green'>handling uncertainty</font> and randomness. It combines principles from probability theory and programming to build systems that can reason about uncertain data and make informed decisions. This approach allows developers to express complex models in a natural and intuitive way, enabling tasks such as Bayesian inference, machine learning, and statistical analysis to be performed more effectively.

Probabilistic programming lies at the intersection of such domains as machine learning algorithms, statistics, and programming laguages, and its golas are to 

- simplify the inference process,
- automate inference.

You can think of the overall logic hierarchy as

Inference &rarr; Probabilistic Programming System   &rarr;  Probabilistic Programming Language  &rarr; Models  &rarr; Applications


## Why do we need probabilistics programming

Because writing your own sampler for Bayesian inference in hard! It involves complex mathematics, knoweldge and understanding of sampling algorithms - both MCMC and approximate, there are potential issues with numeric stability and computational cost. Hence, one needs to be both an excellent developer, as well as an expert statistician to succeed at this task.

Wouldn't it be wonderful to oursouce all these tasks to someone, so that we could focus on solving scientific problems?

## Probabilistic programming languages (PPLs)

In this section we will give an overview of the modern landscape of <font color='orange'>probabilistic programming languages (PPLs)</font> and in the next section we will explore abilities of one of them. Familiarity with a PPL will equip participants with a tool allowing them to <font color='green'>focus on the scientific problem</font> of interest, while inference is being taken care of by the inference engine. For this purpose, we will intorduce the [NumPyro](https://num.pyro.ai/en/latest/index.html#) library to perform exact Bayesian inference (using Markov Chain Monte Carlo).


A PPL allows us to formalize a Bayesian model and perform inference with the help of powerful algorithms. **<font color='teal'>A user needs to only formulate the model</font>**, maybe chose a sampler, and "press the inference button".

An operative definition of probabilistic programming is as follows:

*“Probabilistic programs are usual functional or imperative programs with two added constructs:
1. the ability to draw values at random from distributions, and
2. the ability to condition values of variables in a program via observations.”*
Gordon et al, 2014

Some (relatively) early Probabilistic programming languages and tools, such as BUGS and WinBUGS, showed the way. They had the three key capabiltiies:

- `random` to make random variables
- `constraint` to constraint variables e.g. to data
- `infer` - returns the dsitribution of a variable




The list of currently existing PPLs is overwhelmingly long and only keeps growing:

- BUGS, WinBUGS, JAGS,
- Stan,
- PyMC3, PyMC4, PyMC,
- Nimble,
- Pyro, Numpyro,
- Edward, TensorFlow Probability, Edward 2,
- Gen,
- Turing,
- Stheno,
= SOSS,
- Omega,
- Infer.NET

to name a few.

## How to chose a PPL?
- <font color='green'>Functionality</font>: Evaluate the language's functionality by examining the availability of a wide range of probability distributions and samplers,
- <font color='green'>Oppenness to Customization</font>: Consider whether the PPL allows you to define custom probability distributions and samplers,
- <font color='green'>Performance</font>: Some PPLs may offer optimizations or parallel processing capabilities to improve performance,
- <font color='green'>Documentation</font>: The availability of well-documented resources, including official documentation, tutorials, and guides, can significantly impact your learning curve and productivity. A well-documented PPL makes it easier to understand and use its features effectively.
- <font color='green'>Community Support</font>: An active and supportive community can be an invaluable resource when you encounter challenges or have questions while working with the PPL. Community forums, discussion groups, and user-contributed content can provide guidance and solutions. Dedicated meetups and conferences.
- <font color='green'>Integration</font>: Consider whether the PPL can easily integrate with other tools and frameworks you may need for your project. Compatibility with libraries for data manipulation, visualization, or machine learning can streamline your workflow.