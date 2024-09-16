# Bayesian Modelling and Probabilistic Programming with Numpyro and examples from Epidemiology.

Welcome to the course! The course materials are a WORK IN PROGRESS. For the latest version, as the PDF may not render everything correctly, visit <https://elizavetasemenova.github.io/prob-epi/>.

## About the author

These lecture notes were written by Elizaveta (a.k.a. Liza) Semenova. I am a lecturer in Biostatistics, Computational Epidemiology and Machine Learning at Imperial College London. My work is centered around scalable and flexible methods for spatiotemporal statistics and Bayesian machine learning with applications in epidemiology. This course is meant to set you up well for doing similar research. 

Most recently, my focus has been on using deep generative modelling to power MCMC inference in classical spatial statistics, as well as adaptive survey design. Even though this course does not touch these subjects, feel free to reach out to discuss. 

More details about my work are available [here](https://www.elizaveta-semenova.com/).


## Giving feedback

After the course, I plan to keep improving and expanding the materials since they will be helpful for future students and collaborators.

- To correct typos, please make pull requests on [GitHub](https://github.com/elizavetasemenova/prob-epi). If these notes ever get published, I will list your name in Acknowledgements.

- For more substantial suggestions about the course content, such as desired topics, please use issues on [GitHub](https://github.com/elizavetasemenova/prob-epi) or email them to `elizaveta [dot] p [dot] [insert my surname] [at] gmail [dot] com`.

```{margin}
Acknowledging here that learning does not always have to be enjoyable.
```
- If you enjoyed the content **and / or** learnt from it, please leave a 'star' to the [book's GitHub](https://github.com/elizavetasemenova/prob-epi) repository. 

- If you are creating a written document (a paper, report, book chapter) where you use what you've learnt here, please cite

```
@book{semenova24,
  author = {Semenova, Elizaveta},
  title = {Bayesian Modelling and Probabilistic Programming with Numpyro and examples from Epidemiology.},
  year = {2024},
  source = {https://elizavetasemenova.github.io/prob-epi},
  doi = {https://doi.org/10.5281/zenodo.11550659}
}
```

## Conda environment

To run the code examples from the course, the recommended Conda environment can be created as follows:

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
