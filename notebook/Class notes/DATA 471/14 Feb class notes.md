>[!note]
>Missed yesterday, potentially going to be lost...

- last day on SVMs
- paper 2 posted last night!
	- using chatgpt in the process
		- gloves are off
- performance metrics starting Mon!
- Prog 1 due week from today
	- pain

- parametric
	- train with the primal or dual problems
		- alpha $\to$ w,b
		- $w = \sum_{i=1}^N \alpha_iy_ix_i$
		- $b = y_i w^T x_i$
		- $h(x)=sign(w^Tx+b)$
- non-parametric
	- dual only
	- $\to \alpha$
	- Using the $w$ summation in place of $w$ in $b$ and $h(x)$ instead of pre-building
- multiclass version: two types
	- one-vs-rest
		- train C binary classifiers (each class $i$ vs all others)
		- take the one with the highest score: non-parametric solution w/o sign()
		- downsides:
			- asymmetric classes, more -1 than 1
			- C times more costly than binary, computational intensity
	- one-vs-one
		- train $c(c-1)/2$ classifiers, one for each pair of classes
		- $h(x)$ evaluates on all of the classifiers, picks the class with the most votes
			- first past the post - alt. vote version?
			- tiebreakers via a primary/general election system
		- drawbacks
			- breaking ties
			- loads of evals
- i.g. generally useful when $N$ is small
- 