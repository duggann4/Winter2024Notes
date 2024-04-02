Clustering: Picking $K$:
- Manual cop-outs
	- visual inspection if low-dimensional
	- inspecting cluster members and stats
	- expert knowledge (supercedes)
		- based on how much you know about the data
	- downstream supervised tasks (clustering as an intermediate)
	- elbow method(s)
		- distortion on y, $K$ on x axes, ideally has a sharp bend in the graph
- silhouette score (out of scope)
	- how good is a cluster?
- spectral clustering eigenvalue gap (also out of scope)
	- connected to SSA?
continuous vs discrete

# Density estimation
sibling to clustering
- estimating a probability density function of $x$ from some set
- unsupervised, probalistic, (usually) generative
Why?
- understanding the data
- sampling from it
	- e.g. this person does not exist
- anomaly detection
	- fraud detection
Focusing on normal and gaussian-mixture distributions
- a convenient assumption, flexible
- T distribution
- multivariate normal distributions are things that exist ($\Sigma$ covariance matrix)
	- refer to Math 456 notes
- If $x_i$ and $x_j$ are independent, then $E[x_ix_j]  = E[x_i]E[x_j]=0$
- 