---
aliases: [Scaled Dot-Product Attention]
tags: [machine_learning]
---
# Scaled Dot-Product Attention

Scaled dot-product [[attention]] is the method of attention proposed by [@vaswaniAttentionAllYou2023]. 

Let

$$
\begin{aligned}
q, k \in \mathbb{R}^{d_k} \\
v \in \mathbb{R}^{d_v}
\end{aligned}
$$

where $k$, $q$ and $v$ refer to the key, query, and value vectors respectively, and $d_k$ and $d_v$ refer to the dimensions of the key and value vectors.

Scaled dot-product attention is defined as:

$$
\text{Attention}(q, k, v) = \text{Softmax}\left(\frac{qk^T}{\sqrt{d_k}}\right)v
$$

In matrix form, this can be expressed as 
$$
\text{Attention}(Q, K, V) = \text{Softmax}\left(\frac{QK^T}{\sqrt{d_k}}\right)V
$$

where the matrices $Q$, $K$, $V$ are the stacked vectors. 

>[!info]
> The main contribution here is the *scaling* by $1/ d_k$. The authors found this improves the performance of dot product attention, as at higher dimensions the softmax function will have smaller gradients.

## References

[[@vaswaniAttentionAllYou2023]]
