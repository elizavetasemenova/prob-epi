# Bayesian Modelling and Probabilistic Programming with Numpyro, and Deep Generative Surrogates for Epidemiology.

Welcome to the course! The course materials are a WORK IN PROGRESS. If you are using the PDF, please refer to the online content at <https://elizavetasemenova.github.io/prob-epi/> for the latest updates, as the PDF may not render everything accurately.

## About the author

These lecture notes were written by <span style="color:orange">Elizaveta Semenova</span> (a.k.a. Liza). I am a lecturer in Biostatistics, Computational Epidemiology and Machine Learning at Imperial College London. My work is centered around scalable and flexible methods for spatiotemporal statistics and Bayesian machine learning using probabilsitic programming with applications in epidemiology. This course is meant to set you up well for doing similar research. 

Most recently, my focus has been on using deep generative models to power MCMC inference in classical spatial statistics. It turns out that the same method works for a much wider range of applications, including disease transmission modelling! In part, this course does touch on these topics. Feel free to reach out to discuss the broader landscape of research. 

More details about my work are available [here](https://www.elizaveta-semenova.com/).


## Giving feedback

After delivering the course, I plan to keep improving and expanding the materials since they will be helpful for future students and collaborators.

- To correct typos, please make pull requests on [GitHub](https://github.com/elizavetasemenova/prob-epi). If these notes ever get published, I will list your name in Acknowledgements.

- For more substantial suggestions about the course content, such as desired topics, please use issues on [GitHub](https://github.com/elizavetasemenova/prob-epi) or email them to `elizaveta [dot] p [dot] [insert my surname] [at] gmail [dot] com`.

```{margin}
"and/or" is to acknowledge that learning does not always have to be enjoyable.
```
- If you enjoyed the content **and / or** learnt from it, please leave a 'star' to the [book's GitHub](https://github.com/elizavetasemenova/prob-epi) repository. 

- If you are creating a written document (a paper, report, book chapter) where you use what you've learnt here, please cite 

```
@software{Semenova_Bayesian_Modelling_and_2024,
author = {Semenova, Elizaveta},
doi = {10.5281/zenodo.11550659},
month = jun,
title = {{Bayesian Modelling and Probabilistic Programming with Numpyro and examples from Epidemiology.}},
url = {https://github.com/elizavetasemenova/prob-epi},
version = {v1.0.0},
year = {2024}
}
```

## Conda environment

To run the code examples from the course, you could either download separate notebooks and run them on Colab, or exxecute the notebooks locally. The recommended Conda environment can be created as follows:

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

%## Table of contents

%```{tableofcontents}
%```
