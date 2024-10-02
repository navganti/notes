---
aliases: [Perturbation Model]
tags: [SLAM]
---
# Perturbation Model

In order to find the the optimal rotation or transformation to minimize our least squares error, we will have to take the derivative of a [[lieGroup|Lie group]] element. It is preferred to use the [[lieAlgebra|Lie algebra]], as the optimization can then be unconstrained.

A perturbation model lets us numerically measure changes to the cost function due to an infinitesimal change to the Lie group element. This is done by left-multiplying the  [[mathGroup|group]] element by a perturbation, and then taking the derivative with respect to that perturbation.

>[!note]
>The perturbation model is preferred over the derivative model, as we do not require the Jacobian.

![[gaoIntroductionVisualSLAM2022_001.png]]

For $SO(3)$, this results in a 4x6 Jacobian.

## Related

## References
[[@gaoIntroductionVisualSLAM2022]]
