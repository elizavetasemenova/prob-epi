# Introduction to Modelling in epidemiology

In this course we will consider a range of models used in epidemiology - from <font color='orange'>hierarchical modelling</font> and <font color='orange'>spatial statistics</font> to <font color='orange'>disease transmission modelling</font> - and their probabilistic formulation. In order to perform Bayesian inference we will use the probabilistic programing language (PPL) Numpyro.

Let's uncover each of the three key terms of the course - **epidemioligy**, **Bayesian modelling** and **probablistic programming**. You can think of them as the 'What?', 'Why?' and 'How?' of the course, correspondingly.

(epidemiology)=
## Epidemiology

Epidemiology is the 'What?' of this course, i.e. 'What real-life phenomena do we want to study?'

The range of computational models which we will cover is motivated by questions in epidemiology and public health.

Epidemiology is the study of how diseases and health-related events are distributed within populations and the factors that influence these distributions. It is a branch of public health that focuses on understanding the patterns, causes, and effects of diseases and health conditions on a large scale. Epidemiologists collect and analyze *data* to investigate the occurrence of health outcomes, their risk factors, and the impact of various interventions or preventive measures.

Epidemiological studies are essential for understanding the health of populations, identifying health disparities, and guiding public health efforts to improve the well-being of communities and societies.

Key aspects of epidemiology include:

- **Disease Surveillance:** Epidemiologists <font color='orange'>monitor</font> the occurrence of diseases and health-related events over time and across different geographic areas. This involves tracking the number of cases, identifying outbreaks, and assessing trends in disease incidence and prevalence.

- **Outbreak Investigation:** Epidemiologists are often involved in <font color='orange'>investigating</font> disease outbreaks, such as foodborne illnesses, infectious disease outbreaks, or clusters of chronic diseases. They work to identify the source of the outbreak and implement measures to contain and prevent further spread.

```{margin}
It is important to distinguish <font color='orange'>associative</font> stidies with those where researchers try to oncover <font color='orange'>causal</font> relashionships between risk factors and outcomes.
```
- **Identifying Risk Factors:** Epidemiological studies aim to identify the <font color='orange'>factors</font> that are <font color='orange'>associated</font> with increases likelihood of developing a particular disease. These risk factors can include genetic predisposition, environmental exposures, lifestyle choices, and social determinants of health.

- **Disease Prevention and Control:** The insights gained from epidemiological research are crucial for designing and implementing public health <font color='orange'>interventions</font> and <font color='orange'>policies</font> aimed at preventing and controlling diseases. This may involve vaccination campaigns, health education programs, quarantine measures, and more.

- **Public Health Planning:** Epidemiological data and findings play a vital role in informing public health planning and <font color='orange'>resource allocation</font>. This includes assessing healthcare needs, identifying at-risk populations, and developing strategies to improve overall health outcomes.

- **Causality Assessment:** Epidemiologists use various study designs, including cohort studies, case-control studies, and randomized controlled trials, to determine if a specific factor or intervention <font color='orange'>causes</font> a particular disease.

- **Epidemiological Models:** Mathematical and statistical models are frequently used in epidemiology to simulate <font color='orange'>disease spread</font> and estimate <font color='orange'>disease distribution</font>. These models help in making informed decisions and planning interventions.

Some models that we will build in this course are more relevant to **infectious**, and some to **chronic** diseases. The scope of applicability will be clarified for each model when it is introduced. 

## Bayesian modelling

```{margin}
You musy have hearda lot recently about <font color='orange'>generative AI</font> and <font color='orange'>deep generative modelling (DGM)</font>. It is indeed the same 'generative' idea as we are talking here about. The difference is that DGM uses deep learning and neural network for the generative mechanism, and in traditionla epidemioligy it is more common to use statistical and mechanistic models for such generation. Having said that, we will DGMs in this course too.
```
Bayesian modelling is the 'How?' of this course, i.e. 'How can we describe the <font color='orange'>generative process</font> leading to the data we observe?'. We will use the term 'Bayesian' and 'probabilistic' interchangeably.

Probabilistic modeling is a mathematical and statistical framework used to incorporate **uncertainty** and **randomness** into models to account for variability and its sources in real-world phenomena. It involves using probability theory to describe and quantify the uncertainty associated with different events, outcomes, or variables. The primary goal of probabilistic modeling is to make predictions, infer information, or make decisions in situations where there is inherent uncertainty. Probabilistic modeling is a powerful tool for dealing with real-world complexities in a quantitative manner. It plays a crucial role in data analysis, machine learning, and decision-making processes where probabilistic reasoning is necessary.

Probabilistic modelling in epidemiology helps epidemiologists and public health officials make informed decisions by <font color='orange'>quantifying uncertainty</font>, simulating realistic disease dynamics, and assessing the potential impact of various interventions. It is a powerful tool for improving our understanding of health outcomes and guiding effective public health responses.

%Here's why probabilistic modelling is important for epidemiology:

%- **Capturing Uncertainty:** Epidemics are inherently uncertain processes influenced by numerous variables, including human behavior, environmental factors, and the biology of the infectious agent. Probabilistic models allow epidemiologists to account for this uncertainty by representing it explicitly. This is particularly important when making predictions or assessing the effectiveness of control measures.

%- **Realistic Simulations:** Probabilistic models simulate disease spread and transmission more realistically by considering the variability in individual interactions, susceptibility, and infectiousness. This realism helps in better understanding the dynamics of epidemics and how they may evolve over time.

%- **Data Integration:** Epidemiological data often contain inherent variability and noise. Probabilistic models can incorporate this variability and provide a framework for data assimilation and model calibration. This helps in refining models to fit observed data more accurately.

%- **Quantifying Risk:** Probabilistic models can quantify the likelihood of various outcomes, such as the probability of an outbreak occurring, the probability of disease transmission in a specific setting, or the probability of a particular intervention's success. This information is essential for risk assessment and decision-making.

%- **Scenario Analysis:** Epidemiologists can use probabilistic models to explore a wide range of scenarios and assess the potential impact of different interventions and policies. This aids in designing effective strategies for disease control and prevention.

%- **Sensitivity Analysis:** Probabilistic modelling allows for sensitivity analysis, which helps identify which parameters or assumptions in the model have the most significant impact on outcomes. This information guides research priorities and resource allocation.

%- **Incorporating Individual-Level Variation:** Probabilistic models can capture individual-level variations in disease transmission, susceptibility, and response to interventions. This is crucial for tailoring public health measures to different population segments.

%- **Policy Decision Support:** Probabilistic modelling provides decision-makers with valuable insights into the expected outcomes of different policy choices. This aids in prioritizing resource allocation and optimizing public health interventions.

%- **Adaptability:** As new data becomes available during an epidemic, probabilistic models can be updated and refined, allowing epidemiologists to continuously monitor and adapt their strategies in response to changing circumstances.

Some key concepts and components of probabilistic modeling are as follows:

- **Random Variables:** In probabilistic modeling, random variables are used to represent uncertain quantities or events. These variables can take on different values with associated probabilities.

- **Probability Distributions:** A probability distribution describes how the values of a random variable are distributed or spread out. Common probability distributions used in epidemiological modelling include the normal distribution, binomial distribution, Poisson distribution, and many others. 

- **Parameters:** Probability distributions are often characterized by parameters that determine their shape and behavior. For example, the mean and standard deviation of a normal distribution are parameters that describe its central tendency and spread.

- **Bayesian Inference:** Bayesian probabilistic modeling is a framework that uses Bayes' theorem to update the probability distribution of a random variable based on new evidence or data. It combines **prior beliefs** (prior distribution) with observed data to form a **posterior distribution**, which represents the updated beliefs.

- **Monte Carlo Methods:** Monte Carlo methods are a class of computational techniques used to estimate complex probabilistic models through random sampling. They involve generating random samples from probability distributions to approximate quantities of interest.


## Probabilistic programming


Probabilistic programming is a specialized approach to building and analyzing probabilistic models that offers several advantages for epidemiology and the study of infectious disease dynamics:

- **Flexibility:** Probabilistic programming languages, such as Stan, Pyro, or Edward, provide a flexible framework for defining and customizing probabilistic models. This flexibility is crucial in epidemiology, where the complexity of disease transmission models can vary widely depending on the specific disease and the population under study.

- **Uncertainty Quantification:** Probabilistic programming allows for the explicit representation and quantification of uncertainty. Epidemiological models often involve uncertain parameters and data, and probabilistic programming makes it easier to incorporate this uncertainty into the modelling process.

- **Bayesian Inference:** Probabilistic programming languages are particularly well-suited for Bayesian inference, which is a powerful statistical approach used in epidemiology. Bayesian methods enable the estimation of model parameters, predictions, and model comparisons while accounting for prior information and uncertainty.

- **Model Validation:** Probabilistic programming facilitates model validation by enabling researchers to compare model predictions with observed data using techniques like posterior predictive checks. This helps ensure that models accurately capture the underlying dynamics of infectious diseases.

- **Hierarchical modelling:** Many epidemiological models involve hierarchical structures, where data at multiple levels (e.g., individuals, households, communities) are analyzed simultaneously. Probabilistic programming makes it easier to specify and fit hierarchical models, which can provide more accurate representations of complex disease transmission processes.

- **Data Integration:** Probabilistic programming allows for the integration of various types of data sources, including clinical data, epidemiological surveillance data, and genomic data. This integration can improve the accuracy and informativeness of epidemiological models.

- **Model Selection and Comparison:** Epidemiologists often need to compare different model structures or assess the fit of alternative hypotheses. Probabilistic programming facilitates model selection and comparison through techniques like Bayesian model averaging and model evidence calculation.

- **Real-time Updates:** In the context of infectious disease outbreaks, probabilistic programming allows for real-time updates of models as new data becomes available. This adaptability is critical for guiding public health responses during rapidly evolving situations.

- **Transparent Communication:** Probabilistic programming encourages transparency in modelling and analysis. Researchers can clearly specify their assumptions, priors, and likelihood functions, making it easier to communicate and collaborate with other experts and stakeholders.

- **Extensible Libraries:** Probabilistic programming languages often come with extensive libraries and tools for model development, inference, and visualization, reducing the implementation and computation burden for epidemiologists.

In summary, probabilistic programming is a valuable tool for epidemiologists because it offers a flexible and powerful framework for modelling disease dynamics, quantifying uncertainty, and making data-informed decisions. It enhances the precision and transparency of epidemiological research, ultimately contributing to better public health outcomes.