# Admin notes
- Last quiz!!!
- paper 2 revs due tomorrow...
- prog grades definitely by sun night
- weights-and-biases visuals?
# ML exp
## Splitting data
Recall: Randomly splitting data at some ratio (e.g. 80/10/10)
- Conciderations:
	- avoid testset leakage into train or dev
		- test set is supposed to be new data
			- duplicate points
			- overlap of slices
			- correlation; close in time or space (generalization of ARMA)
	- claims of generalization
		- via your splits, what did your model *actually learn*?
		- different kinds of "new"
		- control variables, environmental factors
		- can have multiple test sets
		- How blind do you fly?
	- sufficient size in each split
## Results and analyses
### Presenting results
- tables and figures quantifying performance
- use test
- don't use too many sig. figs; 3 digits
- statistical significance nice, but not common
### Analyses
- understanding impacts of decisions or gain insight
	- Ablation study: effect of independent decisions, disabling one thing at a time - dishonest...
	- effect of hyperparameters
	- visualizations of what the model learned
		- A fun example: word embeddings