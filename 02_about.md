# About this course

This course will be taught during three weeks from 25 March to 12 April 2024 to a MSc ["AI for Science"](https://ai.aims.ac.za/) cohort at the [African Institute for Mathematical Sciences (AIMS)](https://aims.ac.za/), South Africa.

If you notice any typos, mistakes or inconsistencies in these course notes, please email them to `elizaveta [dot] p [dot] [insert my surname] [at] gmail [dot] com`.

Tentative outline of the course is presented below but might be adjusted during the course.


* <span style="color:orange">Week 1 - Probabilistic programming</span>.
    * Day 1
        * Introduction to modelling in epidemiology
        * Probability distributions refresher
        * Bayesian inference
        * Focus on priors
    * Day 2
    	* numerical methods to obtain posterior
	    * MCMC by hand
	    * convergence diagnostics
	    * PPLs
	    * Intro to Numpyro: model, inference, check convergence
	    * Bayesian workflow: prior predictive and posterior predictive
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


