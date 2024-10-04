---
aliases: [Quadratic Programming]
tags: [math, optimization]
---
# Quadratic Programming

Quadratic programming is the process of optimizing a *quadratic* objective function, subject to *linear* constraints. It is a type of nonlinear programming.  Similar to [[linearProgramming|Linear Programming]], the constraints prohibit the optimal result from reaching $\pm\infty$. 

Quadratic functions will typically be bounded in one direction.
 
$$
\begin{array} \\
    \min\limits_x & q(x) = \frac{1}{2}x^TGx + c^Tx \\
    \text{subject to} & a_i^Tx = b_i, &i \in \mathcal{E}, \\
    & a_i^Tx \ge b_i, & i \in \mathcal{I} \\
\end{array}

$$
When $G$ is symmetric and positive definite, this is the same as a [[leastSquaresProblems|least squares problem]].

## References

[[@nocedalNumericalOptimization2006]]
