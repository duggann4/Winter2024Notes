Project reports due in 12 days - Wed of dead week
# Picking models (considerations)
the models to try first, but no guarantees - flowcharts exist online
```
Size of $N$:
	large (100k+):
		NNs
	medium (1k-100k):
		trees & forests (T&F)
	small (1k-):
		SVMs, linear models, K-NNs
Dimension of features ($D$)
	high (10k+):
		SVMs, *kinds* of NNs (CNNs, etc.), DimReduction (random projection)
	medium (50-10k?):
		NNs
	low (50-):
		T&F, K-NNs?
Complexity of the problem (non-linearity):
	high (images):
		NNs - can scale up, assuming $N$ big enough
		K-NNs
	medium:
		non-linear SVM, T&F
	low:
		linear SVM, other linear models
```

# Baselines
Defining "good" - models/rules to compare to
- *Be* the baseline

Bare minimum:
- Classification: majority class baseline ($\bar{\mu_C}$)
- Regression: training set mean target ($\bar{\mu_{TR}}$) ($R^2=0$)

Others:
- linear model (if working with NNs)
	- otherwise less-powerful models
- strong model from another family
- research: state-of-the-art
- gold standards from outside of ML
	- meteorology - compute power improvements

Tune them fairly (their own hyperparameters)!

# Tuning
Two common sources of h-params:
- model (e.g. numlayers)
- optimizer (e.g. learnrate, mbsize)
Types of h-params:
- continuous (learntate)
- discrete (numunits)
- categorical (actfn)
Searches:
- grid search
	- brute force
	- nested for-loop, easy to implement
	- slow
- random search
	- better than grid
	- getting to better areas of the h-param space quicker
- quasi-random
	- reducing redundancy
- guided
	- modelling the model's h-params

- 