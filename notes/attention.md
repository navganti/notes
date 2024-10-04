---
aliases:
  - Attention
tags:
  - machine_learning
---
# Attention

The goal of attention is to map a key and value pair with a query to an output, where  $q, k, v, o$ are all vectors.

The output is a weighted sum of the values. There are several different ways to do this, including additive attention or [[scaledDotProductAttention|scaled dot-product attention]].

There are two commonly referenced types of attention - *self-attention* and *cross-attention*.

In self-attention, all $k, v, q$ comes from the same tokens. This is used in the attention mechanism within the encoder layers of a [[transformer]].

>[!Example]
>The quick brown fox jumped over **the** lazy **dog**.

In cross-attention,  $q$ is not from the same tokens as $k, v$. In the transformer, there is both a cross-attention and self-attention layer present in the decoder. For cross-attention, the  queries come from the previous decoder layer, but the keys and values come from the encoder output.  This allows the decoder to attend over all positions of the input.

## References

[[@vaswaniAttentionAllYou2023]]
