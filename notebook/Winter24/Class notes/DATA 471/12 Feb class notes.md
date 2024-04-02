Zoom day...

Paper 2 posting tomorrow, next Sat

- soft margin SVMs, non-separables
- pretending that problematic points don't exist
- need to drag points distance $\xi$ to make them not off-side
	- we want a big $m$, but a small sum of $\xi$ values
	- $\arg \min_{w, b, \xi}\frac{1}{2}||w||^2 + C \sum_{i=1}^N \xi_i st y_i(w^Tx_i+b) \geq 1-\xi_i$
		- $/xi$ non-negatives
	- two kinds of support vectors:
		- $\alpha_i>0$ and on margin
		- $\alpha_i>0$ and off-sides ($\xi_i>0$)
- recall that w is a weighted combo of vectors
- 