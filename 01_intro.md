# Bayesian Modelling and Probabilistic Programming with Numpyro and examples from Epidemiology.

Welcome to the course! The course materials are a work in progress. For the latest version, as the PDF may not render everything correctly, visit <https://elizavetasemenova.github.io/prob-epi/>.

## About the author

These lecture notes were written by Elizaveta (a.k.a. Liza) Semenova. I am a lecturer in Biostatistics, Computational Epidemiology and Machine Learning at Imperial College London. My work is centered around scalable and flexible methods for spatiotemporal statistics and Bayesian machine learning with applications in epidemiology. This course is meant to set you up well for doing similar research. 

Most recently, my focus has been on using deep generative modelling to power MCMC inference in classical spatial statistics, as well as adaptive survey design. Even though this course does not touch these subjects, feel free to reach out to discuss. 

More details abot my work are avialable [here](https://www.elizaveta-semenova.com/).


## Giving feedback

To correct typos, please make pull requests on [GitHub](https://github.com/elizavetasemenova/prob-epi). If these notes ever get published, I will list your name in Acknowledgements.

For more substantial suggestions about the course content, such as desired topics, please use issues.


If you enjoyed and/or learnt from these materials, please leave a star on GitHub and/or cite

```
@book{semenova24,
  author = {Semenova, Elizaveta},
  title = {Bayesian Modelling and Probabilistic Programming with Numpyro, and examples from Epidemiology.},
  year = {2024}
}
```

## Conda environment

To run the code examples from the course, the recommended Conda environemnt can be created as follows:

```
conda create -n aims python=3.9
conda activate aims
conda install -c conda-forge jupyter-book
conda install conda-forge::matplotlib
conda install numpy
conda install conda-forge::ghp-import
conda install conda-forge::numpyro
conda install conda-forge::jax
pip install sphinxcontrib-tikz
conda install conda-forge::geopandas
conda install conda-forge::arviz
conda install anaconda::seaborn
pip install pyppeteer
```

## Table of contents

```{tableofcontents}
```