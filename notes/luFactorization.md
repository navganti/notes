---
aliases: [LU Factorization, LU Decomposition]
tags: [math]
---
# LU Factorization

LU factorization decomposes a matrix as follows:

$$
PA = LU
$$

where $L$ is lower triangular and $U$ is upper triangular. The LU factorization can be used to solve a linear system $Ax = b$.

1. Permute $b$: $\hat{b} = Pb = PAx = Gx$
2. Perform forward substitution to solve for $y$: $Gx = L(Ux) = Ly = \hat{b}$
3. Perform back substitution to solve for $x$: $Ux = y$

- LU factorization is the matrix form of Gaussian Elimination. 
    - The method above uses *partial* row pivoting.
    - Full pivoting would include a row and column permutation: $PAQ = LU$
        - Column pivoting does not help stability, but could aid performance if $A$ is sparse.
- Without row exchanges, the elimination of $A$ is described by multiplying $A$ with elimination matrices.
- This can also be applied to non-square matrices, if $m > n$. Else: $PA^T = [L1,\; L2]^T \; U$

>[!example]
>![[mitopencoursewareFactorizationLU2017_001.jpg]]

## Related
[[matrixFactorization|Matrix Factorization]]
[[choleskyFactorization|Cholesky Factorization]]
[[qrFactorization|QR Factorization]]

## References

[[@nocedalNumericalOptimization2006]]
[[@strangFactorizationLU2017]]