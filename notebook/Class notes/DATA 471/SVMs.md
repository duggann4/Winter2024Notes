- talking about Prog 1 tomorrow probably
Going back to first thinking about linear functions

# Support Vector Machines
- a new class of models
- basic form: supervised, linear, binary classifier for linearly seperable data
	- linearly seperable: There exists a plane that can divide the classes
	- later on going to break the lin-sep assumption then linear and multi-class generalization
- 1990s, early 2000s
	- window of coolness
- underlying ideas can be embedded elsewhere
- convention: labels for classes are -1, 1
- NO:
	- sigmoid
	- cross-entropy
	- minimizing emperical risk
- considering margins around hyperplanes such that there are no points within a margin of the bound
- margin:
	- region around the hplane with no points in it
	- one-sided width $m$ of that region
- larger margins = more robust to noise
- Ultimate goal: maximize $m$
- plane at $h(x)=0$
- assuming we get the $m$ of a given hplane automagically
- non-parametric
Translating feelings to math
- $\frac{rise}{run}$
- rephrase run to $m$; $wm=rise=h(x)$
- Normalize using "all-over"
- $y_i\frac{w^Tx_i+b}{||w||} \geq m \forall i$
	- phobia of points
- preliminary optimization problem
	- $argmax_{w,b,m}m s.t. y_i\frac{w^Tx_i+b}{||w||} \geq m \forall i$
	- problem: our definition is self-scaling, thus inf solns
	- fix $m=\frac{1}{||w||}$, makes math easier...
	- 