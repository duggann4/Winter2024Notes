## Example
General schematic: Going from a training set $x$ to a model $h$. Goal is $h(x)=y$

Example: Predicting crime rates given per capita income. $R \to R$
Supervised learning, so data is I/O pairs
$n=5$ is terrifyingly small. Usually on the million order of magnitude.

Procedure:
1. Pick a model family, e.g. linear regression ($h(x)=mx+b$, $m,b$ are parameters/weights)
2. Find optimal function in the family (training)
	1. Define loss function $L(h(x),y), L\geq0, L(a,a)=0$ that tells us how much error is in a prediction. e.g. squared error loss $(h(x)-y)^2$, but this is not the only one, depending on needs
	2. Emperical risk: average loss over the training set. $\hat{R}(m,b) = \frac{1}{N}\sum_{i=1}^N L(h(x_i), y_i)$
	3. Ultimate goal: Find $m, b$ such that $\hat{R}$ is minimized. Unique global minimum of the bowl-shaped 3-space ER function

## Overview
Supervised learning: I have this input and I expect this sort of output
Unsupervised learning: Model only given inputs
Semisupervised: Only some datapoints have outputs given
Last two good example is clustering/labelling
Inputs:
* By convention, $x \in R^D$ is the "feature vector"
* sequences of inputs
* $x \in R^{D_1 \times D_2}$ e.g. image bitmaps, rasters
* structured objects (e.g. trees) (seperate from structured/unstructured data (well-defined fields?))
Feature extraction stuff important, deep-learning can sidestep this (human bias)

Normalization and standardization used to sidestep model scale sensitivities
Supervised outputs:
- $R^C$: regression problems
- categoricals $\{0, 1, \hdots, C-1\}$: classification
- sequence of equal length to input: sequence labelling
- sequence of arbitrary length: decoding (not a standard term, but common in lit)
	- encoder/decoder examples: Image alt text, audio captioning
- ordered list/ordering: ranking
- structured output (e.g. tree): structure prediction

Unsupervised outputs:
- no true outputs...
- arbitrary cluster IDs: clustering (partitioning the input space)
	- Mainly in DL...
- probability/probability density: identifying distributions: density estimation
	- What's "normal"?

Models:
- parametric vs. non-parametric
	- parametric has fixed number of params
	- non-parametric depends on training data, implications on storage space and evaluation stage complexity. e.g. k-nearest neighbors (DL)
- probabalistic vs. non-prob.
	- prob. capable of $P(y\mid x)$
		- subsets: discriminitive ($P(y \mid x$, may be simpler), generative (both sup. and non-sup.) ($P(x,y)$ on $P(x)$, produce samples)
	- non-prob can't.