https://elizavetasemenova.github.io/prob-epi

## Giving feedback

- To correct typos, please make pull requests on [GitHub](https://github.com/elizavetasemenova/prob-epi). If these notes ever get published, I will list your name in Acknowledgements.

- For more substantial suggestions about the course content, such as desired topics, please use issues on [GitHub](https://github.com/elizavetasemenova/prob-epi) or email them to `elizaveta [dot] p [dot] [insert my surname] [at] gmail [dot] com`.

- If you enjoyed the content **and / or** learnt from it, please leave a 'star' to the [book's GitHub](https://github.com/elizavetasemenova/prob-epi) repository. 

- If you are creating a written document (a paper, report, book chapter) where you use what you've learnt here, please cite

```
@software{Semenova_Bayesian_Modelling_and_2024,
author = {Semenova, Elizaveta},
doi = {10.5281/zenodo.11550659},
month = jun,
title = {{Bayesian Modelling and Probabilistic Programming with Numpyro, and Deep Generative Surrogates for Epidemiology.}},
url = {https://github.com/elizavetasemenova/prob-epi},
version = {v1.0.0},
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

## License

<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br />All slides are licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>.