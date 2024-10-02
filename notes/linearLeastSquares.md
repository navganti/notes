---
aliases: [Linear Least Squares]
tags: [math, optimization]
---
# Linear Least Squares

Linear least squares are linear functions of $x$.

$$
\begin{align}
    f(x) &= \frac{1}{2}\|Jx - y\|_2^2 \\
    \nabla f(x) &= J^T(Jx - y) \\
    \nabla^2f(x) &= J^TJ
\end{align}
$$

To find $x^*$:

$$
\nabla f(x) = 0 = J^TJx^* - J^Ty
$$

$$
\therefore J^TJx^* = J^Ty
$$

this is called the *normal equation* for linear least squares. There are three main approaches to solve this.

### Approach 1
1. Compute $J^TJ$ and $J^Ty$
2. Compute the [[choleskyFactorization|Cholesky factorization]] of $J^TJ$
3. Perform the forward and back substitution to isolate $x^*$

The Cholesky factorization is guaranteed to exist when when $m \ge n$ and $J$ has rank $m$. Recall that $m$ is the number of rows due to the total number of residual equations, and $n$ is the dimension of $x$.

**Disadvantage**: The [[conditionNumber|condition number]] of $J^TJ$ is the square of the condition number of $J$. The relative error of the solution is proportional to the condition number, so as a result this solution may be less accurate.

### Approach 2
1. Compute $J^TJ$ and $J^Ty$
2. Compute the [[qrFactorization|QR Factorization]] of $J^TJ$
3. Perform the requisite substitutions to solve for $x^*$

Unlike [[#Approach 1]], this method does not degrade the conditioning of $J$.

### Approach 3
1. Compute $J^TJ$ and $J^Ty$
2. Compute the Singular Value Decomposition of $J^TJ$
3. Perform the substitutions to solve for $x^*$

This approach should be used if greater robustness is required.

### Trade-offs

These approaches have a trade-off between efficiency and robustness. [[#Approach 1]]  is more efficient, while [[#Approach 3]] is more robust.

## Related

[[leastSquaresProblems|Least Squares Problems]]
[[matrixFactorization|Matrix Factorization]]

## References
[[@nocedalNumericalOptimization2006]]