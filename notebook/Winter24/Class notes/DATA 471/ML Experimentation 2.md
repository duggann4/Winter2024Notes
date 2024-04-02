# Organizing the training process for NNs
- prog 1 checkpoint due tonight!

- Differences between math and programs
	- In math, vectors assumed to be columns, rows in math
	- Can do PA in col vectors, but may be adventageous to do rows
		- rows: minibatching as an NxD matrix (rows x columns)
			- numpy broadcasting of bias vector
- Anatomy of a training loop (for DNNs, NNs, LMs, SGD)
```
def train(): 
	w = init_weights() // all the parameters, if non-convex surface, init to non-zeroes
	foreach epoch:
		foreach MB_x, MB_y in data:
			as = forward(MB_x, w) // feeds through model
			loss = computeLoss(MB_y, as)
			grads = backprop(loss, w, as, MB_y)
			w = update_weights(grads, w)
			if time_to_check_dev?: // PA - -v?: True, else every epoch
				eval(dev)
				if best_dev_results?:
					create_checkpoint(w) // to disk
				if too_long_since_best_dev_results?:
					exit()
	
```
- the other backprop video recomended
- one file only please
- 