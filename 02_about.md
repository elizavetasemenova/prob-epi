# About this course

These lecture notes cover the course which will be taught during three weeks from 25 March to 12 April 2024 to a MSc ["AI for Science"](https://ai.aims.ac.za/) cohort at the [African Institute for Mathematical Sciences (AIMS)](https://aims.ac.za/), South Africa. After the course, I plan to keep improving the materials since they will be helpful for future stundents and collaborators.

If you notice any typos, mistakes or inconsistencies, please email them to `elizaveta [dot] p [dot] [insert my surname] [at] gmail [dot] com`.

We will cover such topics as Bayesian inference, hierarchical modelling, spatial statistics and Gaussian processes, disease transmission modelling and ordinary differential equations. We will build probabilistic models and perform inference using Numpyro in a fully Bayesian manner to characterise uncertainty of the modelled quantities.

Although the course is primarily *compuational* in nature, the models we will examine are inspired by the typical modeling practices found in epidemiology.

Tentative outline of the course is presented below (but might be adjusted during the course).

* <span style="color:orange">Week 1</span>
    * Bayesian inference
    * Probabilistic programming
    * Bayesian workflow
    * Hierarchical Bayesian models
* <span style="color:orange">Week 2</span>
    * Gaussain Processes
    * spatial modelling
    * Bayesian optimisation and active learning
* <span style="color:orange">Week 3</span>
    * infectious disease modelling
    * Deep generative models and how they can help




* <span style="color:orange">Week 1 - Probabilistic programming</span>.
    * Day 1
        * Introduction to modelling in epidemiology
        * Probability distributions and random variables
        * Bayesian inference
        * Focus on priors
    * Day 2
	    * The Monte Carlo methods and MCMC
	    * Convergence diagnostics
	    * Probabilistic programming
	    * Introduction to Numpyro
	    * Bayesian workflow
    * Day 3 
    	* logistic regression with Numpyro
        * Poisson and NegativeBinomial regression with Numpyro
    * Day 4
        * hierarchical modelling
    * Day 5
        * bonus topic: Bayesian neural network with a PPL
        * Practical 1 submission
* <span style="color:orange">Week 2 - spatial modelling</span>.
    * Day 1
        * GPs refresher: MVN, mean, kernel, covariance
	    * kernels: RBF. Matern
	    * non-stationary kernels: linear
	    * combining kernels
	    * scalability: Kronecker
	    * approximations: HSGP
    * Day 2
        * areal data modelling
    * Day 3 
        * geostatistical data modelling
    * Day 4
        * point pattern modelling
        * Practical 2 submission
* <span style="color:orange">Week 3 - infectious disease modelling</span>.
    * Day 1
    	* disease transmission modelling: overview
	    * ODEs
	    * solve ODEs without Numpyro: SIS, SIR, SIRD, SIRS, SEIR, SIRC
	    * (bonus topics: phase portraits, stability)
	    * estimating R_0, R_t
    * Day 2
        * ODEs with Numpyro
        * SIR with Numpyro, boarding school example
    * Day 3 
        * ABMs
        * ABMs on networks
    * Day 4
        * renewal equation
        * Practical 3 submission
    * Day 5
        * Bonus topics: VAEs and diffusion model for prior learning
        * causality


