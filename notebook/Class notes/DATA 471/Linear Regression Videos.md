Useful not only in itself, but also in neural networks (as a layer)

For now, focusing on $c=1$:
> $h(x)=\sum_{i=1}^D w_ix_i+b$
$w$ and $b$ are parameters

Using squared error loss function

Goal: find $w,b$ such that the average loss is minimized

If you can, always shove things into vectors

## SLR

New goal: $argmin_{w,b}1/N(\tilde{X_w}+\tilde{b}-\tilde{y})^T(\tilde{X_w}+\tilde{b}-\tilde{y})$
- $\tilde{X}$ is comprised of input as *row* vectors
- $\tilde{b}$ is bias vector
- $\tilde{y}$ is output vector
Note: The function in new goal is convex and quadratic; will have a global optimal value

Matrix cookbook & derivations for gradient decent
$$\frac{d\hat{R}}{dw}=\frac{2}{N}\tilde{X}^T(\tilde{X_w}+\tilde{b}-\tilde{y})$$
$$\frac{d\hat{R}}{db}=\frac{2}{N}\mathbb{1}^T(\tilde{X_w}+\tilde{b}-\tilde{y})$$
- $\mathbb{1} =$ vector of all ones
Closed-form solution exists! See also: MATH342
- prepending inputs with ones in order to consolidate bias stuff
$$(\hat{X}^T\hat{X})^{-1}\hat{X}^T\tilde{y}$$

## MLR
When $c>1$

Loss function: Square of norm of difference between pred and act

Frobenius norm: Generalization of the L2 norm, square each element and summing each element
$$\frac{\partial \hat{R}}{\partial w}=\frac{2}{N}\tilde{X}^T(\tilde{X_w}+\tilde{B}-\tilde{Y})$$
$$\frac{\partial \hat{R}}{\partial b^T}=\frac{2}{N}\mathbb{1}^T(\tilde{X_w}+\tilde{B}-\tilde{Y})$$

