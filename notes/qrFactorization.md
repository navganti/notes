---
aliases: [QR Factorization, QR Decomposition]
tags: [math]
---
# QR Factorization

QR factorization decomposes a matrix as follows:

$$
AP = QR
$$

where $A$ is square and orthogonal, and $R$ is upper triangular. This can be used to solve linear equations as well, as follows.

1. $Ax = QRP^Tx = b$. Multiply by $Q^T$ on both sides.
2. $RP^Tx = Ry = Q^Tb = \hat{b}$. Solve for $y$ by back substitution.
3. $x = Py$, and solve for $x$ by rearranging.

>[!todo]
>Try to understand QR decomposition better - this note is lacking.

## References

[[@nocedalNumericalOptimization2006]]
