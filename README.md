https://elizavetasemenova.github.io/prob-epi

To correct typos, please make pull requests. If these notes get published, I will list your name in Acknowledgements.

For more substantial suggestions about the course content, such as desired topics, please use issues.

If you enjoyed and/or learnt from these materials, please leave a star on GitHub and/or cite

```
@book{semenova24,
  author = {Semenova, Elizaveta},
  title = {Bayesian Modelling and Probabilistic Programming with Numpyro, and examples from Epidemiology.},
  year = {2024}
}
```

To run the code examples from the course, the recommended environemnt can be created as follows:

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

