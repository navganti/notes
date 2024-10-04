---
aliases: [Transformer]
tags: [machine_learning]
---
# Transformer

The transformer is an architecture introduced by [@vaswaniAttentionAllYou2023]. This network relies on [[attention]] to perform sequence transduction tasks.

![[model_architecture.png]]

This first version of the network proposed is an encoder-decoder architecture with 6 encoder layers and 6 decoder layers.

The encoder has 2 sublayers and uses multi-head attention. This is a self-attention module which uses the input from the previous encoder layer.

The decoder has 3 sublayers; the first is a self-attention module similar to the encoder, but the second is a cross-attention module which uses the encoder output as the queries.

## References

[[@vaswaniAttentionAllYou2023]]
