- program grades getting close... few days until I die...

# Clustering
- unsupervised vs supervised
- coming back to unsupervised
- non-prob today, prb tomorrow and Wed
- Unsupervised: no true labels
	- goal: assign points to clusters that have something similar
- often exploratory
Why?
- finding meaningful structure
	- cross-cutting, but ultimately at the mercy of the algo; strategically creating noise
- As a bad surrogate fo ra classigication task (rare)
	- Can lead the algo to water, but can't force it to drink
- discretize continuous data (vector quantization)
	- lossy compression
Easy in 2D to the brain
- what does a cluster look like?

K-means
- simplest, iterative
- k is num of clusters, a h-param
- steps
	- initialize k centroids
	- while not converged:
		- assign points to centroids ($h(x)=\arg\min_i||x-c_i||^2$) (the closest datapoint)
		- update centroids to better fit their clusters
- convergence: if we're not updating anything - nothing changes in assignment step
- the clustering pattern (formerly decision regions) is lalled a voronoi tesselation

The optimization problem:
$$\arg\min_{c \in C,h} \sum_{x \in X}||x-c||^2$$
non-convex, polygons are a problem...
problem: distortion always encourages larger k