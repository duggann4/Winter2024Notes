- 3 videos on backprop, only need to watch intro
- SVMs mark end of flip
- Programming assignment to post next week, covers up to M4 (inclusive)

# ML Exp. - Preparing data
1. acquiring data
2. splitting into sets
3. preprocessing
4. sanity-checking
## Acquiring
- standard benchmark datasets
	- easy to compare models
	- healthy arms-races
	- focuses on the implementation of the methods
	- e.g.
		- TIMIT, switchboard, etc for speech
		- MNIST, CIFAR, ImageNet, etc for images
- Data collected, but not a benchmark
	- e.g. astronomy, climate
	- files exist, but need to do stuff to it
	- "new" formats: NetCDF, etc.
		- usually python libraries
- Need to collect data
	- Just say "no"
	- good luck
	- web scraping, etc.
- synthetic data
	- manually generated
	- random number generators
	- typically used to test a specific hypothesis in theoretical work
	- a theoretical person trying to get a little emperical
## Splitting
- train/dev/test
- If benchmark, splits provided
	- breaks the purpose
- TR/DV/TE or TR/TE
	- If you want a DV, split TR
	- Be wary of TR/TE, prone to dishonest use
- Else, make your own
	- Simple case: data is independent and homogenous (IID)
		- Roll a d3
		- somewhere between 60/20/20 and 80/10/10
			- x% chance that a given point is in a set
		- *To be continued...*