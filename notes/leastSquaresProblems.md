---
aliases: [Least Squares Problems]
tags: [math, optimization]
---
# Least Squares Problems

All least squares problems are set up with a special form,

$$
f(x) = \frac{1}{2} \sum_{j = 1}^{m}r_j^2(x)
$$

where each $r_j$ is a residual, and $x \in \mathbb{R}^n$. We can convert this to vector form:

$$
\begin{align}
    r(x) &= [r_1(x), r_2(x), \; \dots, r_m(x)]^T \\
    f(x) &= \frac{1}{2} \|{r(x)}\|_2^2
\end{align}
$$

This function has the following Jacobian and Hessian.

$$
\begin{align}
    \nabla f(x) &= J(x)^Tr(x) \\
    \nabla^2f(x) &= J(x)^TJ(x) + \sum_{j = 1}^mr_j(x)\nabla^2r_j(x)
\end{align}
$$

where the Jacobian is evaluated at each measurement. The Jacobian is defined by:

$$
J(x) = \left[\frac{\partial r_j}{\partial x_i}\right]\
\forall \; j = 1\dots m, \; i = 1 \dots n
$$

- The first derivative is easy to calculate, so we therefore can obtain an *approximation* to the Hessian ($J^TJ$) for relatively cheap. 
- The second term of the Hessian is usually negligible, either because $\nabla^2r_j$ is small due to the cost function characteristics, or $r_j$ itself is small.
- Typically assume that measurements are independent and identically distributed (IID), and defined with a variance $\sigma^2$. 

Each residual will now have a probability density function $g_\sigma(\epsilon_j)$ (for example, a Gaussian), where $\epsilon_j$ is defined as:

$$
\epsilon_j = y_j - \phi(x, t_j) = r_j(x)
$$

If all observations are IID, then the probability of the measurements, given the model parameters and variance is defined by the product:

$$
p(y|x, \sigma) = \prod_{j=1}^mg_\sigma(\epsilon_j)
$$

The most likely estimate of x is found by maximizing p. 

$$
\hat{x} = \underset{x}{\operatorname{argmax}}p(y|x, \sigma)
$$

- Probability is associated with the *outcomes*, or $y$, while the likelihood is associated with the *parameters*, or $x$.

The general form of the least squares objective can be expressed as:

$$
r(x)^TWr(x)
$$

where $W \in \mathbb{R}^{m\times m}$ is symmetric. In #SLAM, this is our covariance matrix.

## Related
[[linearLeastSquares|Linear Least Squares]]

## References

[[@nocedalNumericalOptimization2006]]