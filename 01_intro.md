# Bayesian Modelling and Probabilistic Programming with Numpyro, and examples from Epidemiology.

Welcome to the course! The course materials are a work in progress. For the latest version, as the PDF may not render everything correctly, visit <https://elizavetasemenova.github.io/prob-epi/>.

If you enjoyed and/or learnt from these materials, please leave a star on GitHub and/or cite

```
@book{semenova24,
  author = {Semenova, Elizaveta},
  title = {Bayesian Modelling and Probabilistic Programming with Numpyro, and examples from Epidemiology.},
  year = {2024}
}
```

## Conda environment

To run all code examples from the counrse, the recommended environemnt can be created as follows:

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



```{tableofcontents}
```
