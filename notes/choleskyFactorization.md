---
aliases: [Cholesky Factorization, Cholesky Decomposition]
tags: [math, optimization, SLAM]
---
# Cholesky Factorization

If $A$ is positive definite and symmetric, the Cholesky factorization can be computed at $\frac{1}{2}$ the cost of [[luFactorization|LU Factorization]].

$$
\boxed{A = LL^T}
$$

Cholesky decomposition can be used to solve linear equations through forward and back substitution.

1. $Ax = LL^Tx = b$
2. $Ly = b$
3. $L^Tx = y$

Cholesky factorization is very commonly used to solve the SLAM problem, due to the characteristic sparse structure of the Hessian matrix.

## Related
[[matrixFactorization|Matrix Factorization]]
[[qrFactorization|QR Factorization]]

## References
[[@nocedalNumericalOptimization2006]]
