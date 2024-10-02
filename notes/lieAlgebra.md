---
aliases: [Lie Algebra]
tags: [math, optimization, SLAM]
---
# Lie Algebra

The Lie algebra is used to approximate the [[lieGroup|Lie group]] as a first order Taylor series. It can be thought of as a tangent vector at the identity element of the group.

The Lie algebra consists of a set, scalar field, and an operator (the Lie Bracket). The Lie algebra must satisfy the following axioms:

- Closure
- Bilinear Composition
- Reflexive
- Jacobi Identity

The Lie algebra can be converted to the Lie group via the exponential map. For rotations specifically, the exponential map is just the Rodrigues Formula. The transformation also includes a translation parameter, $t = J\rho$. The derivation of this can be found **HERE **.

>[!todo]
>Link the exponential map math derivation for $SE(3)$)

>[!note]
>We want to use the Lie algebra over the Lie group when optimizing for a rotation or transformation variable, because this allows for the optimization to be *unconstrained*. 

## Related
[[bchApproximation|Baker-Campbell-Hausdorff Approximation]]

## References
[[@gaoIntroductionVisualSLAM2022]]
