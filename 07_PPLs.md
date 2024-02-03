# Probabilistic Programming Languages

## Probabilistics programming

[Probabilistic programming](https://en.wikipedia.org/wiki/Probabilistic_programming) (PP) is a paradigm in computer programming that enables the creation of models and algorithms capable of <font color='green'>handling uncertainty</font> and randomness. It combines principles from probability theory and programming to build systems that can reason about uncertain data and make informed decisions. This approach allows developers to express complex models in a natural and intuitive way, enabling tasks such as Bayesian inference, machine learning, and statistical analysis to be performed more effectively.

Probabilistic programming lies at the intersection of such domains as machine learning algorithms, statistics, and programming laguages, and its golas are to 

- simplify the inference process,
- automate inference.

```{tikz, tikz-ex, fig.cap = "Funky tikz", fig.ext = 'png', cache=TRUE}
\usetikzlibrary{arrows}
\begin{tikzpicture}[node distance=2cm, auto,>=latex', thick, scale = 0.5]
\node (P) {$P$};
\node (B) [right of=P] {$B$};
\node (A) [below of=P] {$A$};
\node (C) [below of=B] {$C$};
\node (P1) [node distance=1.4cm, left of=P, above of=P] {$\hat{P}$};
\draw[->] (P) to node {$f$} (B);
\draw[->] (P) to node [swap] {$g$} (A);
\draw[->] (A) to node [swap] {$f$} (C);
\draw[->] (B) to node {$g$} (C);
\draw[->, bend right] (P1) to node [swap] {$\hat{g}$} (A);
\draw[->, bend left] (P1) to node {$\hat{f}$} (B);
\draw[->, dashed] (P1) to node {$k$} (P);
\end{tikzpicture}
```

You can think of the overall logic hierarchy as

Inference &rarr; Probabilistic Programming System   &rarr;  Probabilistic Programming Language  &rarr; Models  &rarr; Applications

In this section we will give an overview of the modern landscape of <font color='orange'>probabilistic programming languages (PPLs)</font> and in the next section we will explore abilities of one of them (NumPyro). Familiarity with a PPL will equip participants with a tool allowing them to <font color='green'>focus on the scientific problem</font> of interest, while inference is being taken care of by the inference engine. 


We will show how to use the [NumPyro](https://num.pyro.ai/en/latest/index.html#) library to perform exact Bayesian inference (using Markov Chain Monte Carlo).

## Probabilistic programming languages (PPLs)

An operative definition of probabilistic programming is as follows:

“Probabilistic programs are usual functional or imperative programs with two added constructs:

1. the ability to draw values at random from distributions, and

2. the ability to condition values of variables in a program via observations.”
Gordon et al, 2014


Luckily, we do not need to write a sampler by hand every time, because PPLs are there to help.

A PPL allows us to formalize a Bayesian model and perform inference with the help of powerful algorithms. **<font color='teal'>A user needs to only formulate the model</font>** and maybe chose a sampler.

Luckily, we do not need to write a sampler by hand every time, because probabilistic programming languages (PPLs) are there to help.

A PPL allows to formalize a Bayesian model and perform inference with the help of powerful algorithms. A user needs to only formulate the model (and maybe chose a sampler) and press the inference button.

The list of currently existing PPLs is overwhelmingly long and only keeps growing:

BUGS, WinBUGS, JAGS,
Stan,
PyMC3, PyMC4,
Nimble,
Pyro,
Edward, TensorFlow Probability, Edward 2,
Gen,
Turing,
Stheno,
SOSS,
Omega,
Infer.NET
to name a few.size(chains)