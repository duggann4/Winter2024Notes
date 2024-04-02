- Final exam review session scheduling survey exists
- final project report tomorrow
# ML Theory Continued
## Recap
**Bayes Decision Rule**
- assumes we have the true distributions
- optimal dividing line to minimize conditional risks
**Bayes Risk**
- lowest risk possible, assuming the true I/O relationship known
- irreducible error
**Bayes Error**
- 0-1 loss

*error vs risk*
## Applying BDR
- If we have $P(x|y)$, we're all set
- if we have $P(x,y)$...
$$P(y|x)=\frac{P(x,y)}{P(x)}=\frac{P(x,y)}{\sum_yP(x,y)}$$
- If we have $P(y|x)$ and $P(y)$...
$$P(y|x)=\frac{P(x|y)P(y)}{P(x)} = \frac{P(x|y)P(y)}{\sum_{y'}P(x|y')P(y')}$$
- bunch of different colors of unicorns

## Reducing irreducible error
How do we reduce the irreducible error?
- more data features
- polynomial feature expansion doesn't help, just identifying combos of features
Problems:
- higher risk solutions overall, more opportunities for issues and overfit
- compute demands

## Curse of Dimensionality
- very difficult to learn "local" phenomena in high-dimensional space
- intuition breaks down; too many if statements
	- volumes of a unit hypercube: $r \to r^{1/D}$
	- hyperballs: how close is the closest point (uniform distribution) to the origin? Medians?
		- pseudo-intuition: volume converges to the surface
Punchlines:
- Interpolation? what's that?
- KNN issues...
- Sampling density needs $O(N^D)$ points
	- All high-dimensional problems are sparse/low-data
		- Turning to SVMs
		- bootstrapping?
		- dimensionality reduction