---
aliases: [Matrix Factorization]
tags: [math, optimization]
---
# Matrix Factorization

Matrix factorization is the process of breaking down a matrix into submatrices. The product of these submatrices will result in the original matrix. Matrix factorization is extremely useful in solving [[leastSquaresProblems| least squares problems]] as decomposing a matrix can lead to a simpler problem than just inverting it.

- All factorizations discussed use a *permutation matrix*.
    - An identity matrix with swapped rows will swap the rows of a *postmultiplied* matrix.
    - An identity matrix with swapped columns will swap the columns of a *premultiplied* matrix

## Related
[[luFactorization|LU Factorization]]
[[choleskyFactorization|Cholesky Factorization]]
[[qrFactorization|QR Factorization]]

## References
[[@nocedalNumericalOptimization2006]]
