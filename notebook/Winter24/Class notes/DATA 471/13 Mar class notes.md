- proj
	- Test set predictions to post at 10
	- have 24 hours to run through model
	- double check formatting
		- sanity check
	- Not a philosophy paper... density
- Packed schedule on Fri, but no new info

# MLT Day 3
### Recap
- Lots of features = lots of problems (See: curse of dimensionality)
- Issues with "mapping down" linearity
### What's the best learning algorithm?
- learning algo.: Bundle of model and training process ($X \to h(x)$)
- Inductive bias: Refers to the assumptions learning algos make to generalize to unseen points (aka how models fill in the gap)
Example: We have some sort of unknown dataset $X$. Let's train it using algo $i$ and $j$, giving models $h_i(x), h_j(x)$ respectively.

Suppose the true relationship is $P_k(x,y)$, thus the model has risk $R_k(h_{[i,j]})$ for uncountably infinite true relationships. Then, the empirical risk $\bar{R}$ is a weighted average over all tasks $R$ weighted by prob of $X$ coming from that task.

$\bar{R}(h_i)=\bar{R}(h_j)$ when averaging over all possible $X$. This is a result of the "no free lunch" theorem.

Implications:
- Absent assumptions about task, no ~~algo~~ (feature representation) is superior
- for any given task, some are better
	- try a lot of options
	- pick approaches based on experience

### What is the best feature representation?
Feature vectors encode similarity and dissimilarity between points; notions of smoothness.
- Similarly, there is no best representation in the task-agnostic context
**Ugly Duckling Theorem:** Any two points can be arbitrarily similar or dissimilar based on feature representation
