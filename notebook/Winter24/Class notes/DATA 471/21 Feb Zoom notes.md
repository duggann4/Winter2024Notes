- prog 1 stuff
- paper 2 exists
- change of plans on Friday
	- Logan Sizemore going to give a lecture on scikit-learn
	- quiz logistics TBD
Pop quiz

F-measure: A combination of precision and recall
$$F_\beta=(1+\beta^2)\frac{PR}{\beta^2P+R}$$

Effect of $\beta$: $F_0 \approx P$, $F_\infty \approx R$

- Macro F1: foreach class m in C, rephrase to detection problems, then take average
	- every class has equal vote
- Micro F1: sum the confusion matrices, *then* compute F1
	- psuedo-weighted average

varying the detection threshold
- screwing around with probability cutoffs
- as $\theta \to 1$
	- recall decreases, precision increases
	- confidence
- $\theta$ is a tunable thing
Regression metrics:
- assuming C=1 for now...
- SSE: sum of squared residuals
- MSE: mean squared error
- RMSE: root MSE
- SAE: sum of absolute error
- MAE: mean abs error
- coefficient of determination ($R^2$)
- 