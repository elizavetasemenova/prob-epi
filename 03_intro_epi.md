# Introduction to Modelling in epidemiology

In this course we will consider a range of models used in epidemiology - from <font color='orange'>hierarchical modelling</font> and <font color='orange'>spatial statistics</font> to <font color='orange'>disease transmission modelling</font> - and their probabilistic (Bayesian) formulation. In order to perform Bayesian inference we will use the probabilistic programing language (PPL) <font color='teal'>Numpyro</font>.

Let's uncover each of the three key terms of the course - **epidemiology**, **Bayesian modelling** and **probablistic programming**. You can think of them as the 'Why?', 'What?' and 'How?' of the course, correspondingly.

(epidemiology)=
## Epidemiology

Epidemiology serves as the underlying rationale in this course, explaining <font color='orange'>WHY</font> we develop the probabilistic models we'll be examining. Essentially, it addresses the question: 'What real-world phenomena are we aiming to analyze using these models?'

<font color='orange'>Epidemiology</font> is the study of how diseases and health-related events are distributed within populations and the factors that influence these distributions. It is a branch of public health that focuses on understanding the patterns, causes, and effects of diseases and health conditions on a large scale. Epidemiologists collect and analyze *data* to investigate the occurrence of health outcomes, their risk factors, and the impact of various interventions or preventive measures.

Epidemiological studies are essential for understanding the health of populations, identifying health disparities, and guiding public health efforts to improve the well-being of communities and societies.

Here is a few examples of epidemiological study types.


```{margin}
If the surveillance tackles purely the temporal development of a health outcome, it suffices to construct temporal models. If space is also of interest, one needs to build spatial or spatiotemporal models.
```
- **Disease Surveillance:** Epidemiologists <font color='orange'>monitor</font> the occurrence of diseases and health-related events over <font color='orange'>time</font> and across different <font color='orange'>geographic areas</font>. This involves tracking the number of cases, identifying outbreaks, and assessing trends in disease incidence and prevalence. Disease surveillance can be conducted for both infectious and non-infectious diseases.

- **Outbreak Investigation:** Epidemiologists are often involved in <font color='orange'>investigating</font> disease outbreaks, such as foodborne illnesses, infectious disease outbreaks, or clusters of chronic diseases. They work to identify the source of the outbreak and implement measures to contain and prevent further spread.

```{margin}
It is important to distinguish <font color='orange'>associative</font> studies with those where researchers try to oncover <font color='orange'>causal</font> relationships between risk factors and outcomes.
```
- **Identifying Risk Factors:** Epidemiological studies aim to identify the <font color='orange'>factors</font> that are <font color='orange'>associated</font> with increases likelihood of developing a particular disease. These risk factors can include genetic predisposition, environmental exposures, lifestyle choices, and social determinants of health.

- **Disease Prevention and Control:** The insights gained from epidemiological research are crucial for designing and implementing public health <font color='orange'>interventions</font> and <font color='orange'>policies</font> aimed at preventing and controlling diseases. This may involve vaccination campaigns, health education programs, quarantine measures, and more.

- **Public Health Planning:** Epidemiological data and findings play a vital role in informing public health planning and <font color='orange'>resource allocation</font>. This includes assessing healthcare needs, identifying at-risk populations, and developing strategies to improve overall health outcomes.

- **Causality Assessment:** Epidemiologists use various study designs, including cohort studies, case-control studies, and randomized controlled trials, to determine if a specific factor or intervention <font color='orange'>causes</font> a particular health outcome.

Mathematical and statistical models are frequently used in epidemiology to simulate <font color='orange'>disease spread</font> and estimate <font color='orange'>disease distribution</font>. These models help in making informed decisions and planning interventions.

Some models that we will build in this course are more relevant to <font color='orange'>infectious</font>, and some to <font color='orange'>chronic</font> diseases. The scope of applicability will be clarified for each model when it is introduced. 

## Bayesian modelling

```{margin}
You must have heard a lot recently about <font color='orange'>generative AI</font> and <font color='orange'>deep generative modelling (DGM)</font>. It is indeed the same 'generative' idea as we are talking here about. The difference is that DGM uses deep learning and neural network for the generative mechanism, and in traditional epidemiology it is more common to use statistical and mechanistic models for such generation. Having said that, we will touch DGMs in this course too.
```
Bayesian modelling represents the fundamental focus of this course, addressing the question of "<font color='orange'>WHAT</font> models can describe the <font color='orange'>generative process</font> behind the observed data?" Throughout the course, we will use the terms "Bayesian" and "probabilistic" interchangeably.

Probabilistic modelling is a mathematical and statistical framework used to incorporate <font color='orange'>uncertainty</font> and <font color='orange'>randomness</font> into models to <font color='orange'>account for variability</font> and its sources in real-world phenomena. It involves using probability theory to describe and quantify the uncertainty associated with different events, outcomes, or variables. The primary goal of probabilistic modelling is to make predictions, infer information, or make decisions in situations where there is inherent uncertainty. Probabilistic modelling is a powerful tool for dealing with real-world complexities in a quantitative manner. It plays a crucial role in data analysis, machine learning, and decision-making processes where probabilistic reasoning is necessary.

Probabilistic modelling in epidemiology helps epidemiologists and public health officials make informed decisions by <font color='orange'>quantifying uncertainty</font>, simulating realistic disease dynamics, and assessing the potential impact of various interventions. It is a powerful tool for improving our understanding of health outcomes and guiding effective public health responses.

Some key concepts and components of probabilistic modelling are as follows:

- **Random Variables:** In probabilistic modelling, random variables are used to represent uncertain quantities or <font color='orange'>events</font>. These variables can take on different values with associated probabilities.

- **Probability Distributions:** A probability distribution describes how the values of a random variable are distributed or <font color='orange'>spread out</font>.

- **Parameters:** Probability distributions are often characterized by parameters that determine their shape and behavior. For example, the mean and standard deviation of a normal distribution are parameters that describe its central tendency and spread.

- **Bayesian Inference:** Bayesian probabilistic modelling is a framework that uses Bayes' theorem to update the probability distribution of a random variable based on new evidence or data. It combines <font color='orange'>prior beliefs</font> (prior distribution) with observed data to form a <font color='orange'>posterior distribution</font>, which represents the updated beliefs.

- **Monte Carlo Methods:** Monte Carlo methods are a class of computational techniques used to estimate complex probabilistic models through <font color='orange'>random sampling</font>. They involve generating random samples from probability distributions to approximate quantities of interest.


## Probabilistic programming


Probabilistic programming is a specialized approach to building and analyzing probabilistic models that offers several advantages for epidemiology and the study of infectious disease dynamics:

- **Flexibility:** <font color='orange'>Probabilistic programming languages</font>(PPLs), such as Stan, Pyro, Numpyro, PyMC, Turing.jl and other, provide a flexible framework for defining and customizing probabilistic models. This flexibility is crucial in epidemiology, where the complexity of disease transmission models can vary widely depending on the specific disease and the population under study.

- **Abstract modelling from inference:** Probabilistic programming languages abstract model formulation from inference. We can <font color='orange'>focus on the applied question</font>, and do not need to write samplers by hand. Instead, we can use robus and tests in battle samples provided by the PPLs.

- **Uncertainty Quantification:** Probabilistic programming allows for the <font color='orange'>explicit representation</font> and quantification <font color='orange'>of uncertainty</font>. Epidemiological models often involve uncertain parameters and data, and probabilistic programming makes it easier to incorporate this uncertainty into the modelling process.


- **Model Validation:** Probabilistic programming facilitates model validation by enabling researchers to compare model predictions with observed data using techniques like <font color='orange'>posterior predictive checks</font>. 

- **Hierarchical modelling:** Many epidemiological models involve <font color='orange'>hierarchical structures</font>, where data at multiple levels (e.g., individuals, households, communities) are analyzed simultaneously. Probabilistic programming makes it easier to specify and fit hierarchical models capturing such structure.

- **Data Integration:** Probabilistic programming facilitates the integration of various types of data. This integration can improve the accuracy and informativeness of epidemiological models.

- **Model Selection and Comparison:** Epidemiologists often need to compare different model structures or assess the fit of alternative hypotheses. Probabilistic programming facilitates model selection and comparison through techniques like Bayesian model averaging and model evidence calculation.

- **Transparent Communication:** Probabilistic programming encourages <font color='orange'>transparency</font> in modelling and analysis. Researchers can clearly specify their assumptions, priors, and likelihood functions, making it easier to communicate and collaborate with other experts and stakeholders.

- **Extensible Libraries:** Probabilistic programming languages often come with extensive libraries and <font color='orange'>tools</font> for model development, inference, and visualization, reducing the implementation and computation burden.



`````{admonition} Task 01
:class: tip
Find a publication that applies Bayesian inference in the field of epidemiology, such as in spatial statistics or disease transmission modeling.

- Identify which Bayesian methods (such as MCMC, VI, ABC, etc) and models were employed in the paper.
- Determine the inference tools applied in the study, such as PPL usage, custom MCMC samplers, or specialized libraries.
- Do you think the modelling part of the study could be improved or extended in some way?
`````