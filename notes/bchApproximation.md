---
aliases: [Baker-Campbell-Hausdorff Approximation]
tags: [math, SLAM]
---
# Baker-Campbell-Hausdorff Approximation

The BCH approximation lets us approximate changes in the [[lieAlgebra|Lie algebra]] due to a change in the [[lieGroup|Lie group]].

The approximation is defined as:
$$
\exp(\Delta \phi^\wedge)\exp(\phi) = exp((\phi + J_l^{-1}(\phi)\Delta\phi^\wedge)) 
$$

or
$$
\exp((\phi + \Delta \phi)^\wedge) = \exp((J_l \Delta \phi)^\wedge)\exp(\phi^\wedge)
$$

Where $J_l$ is the linear left Jacobian found in the $\mathfrak{se}(3)$ exponential map. This is specifically the *left* Jacobian model.

## References

[[@gaoIntroductionVisualSLAM2022]]

