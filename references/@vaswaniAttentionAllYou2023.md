---
# [[@vaswaniAttentionAllYou2023]]
title: Attention Is All You Need
authors:
  - Ashish Vaswani
  - Noam Shazeer
  - Niki Parmar
  - Jakob Uszkoreit
  - Llion Jones
  - Aidan N. Gomez
  - Lukasz Kaiser
  - Illia Polosukhin
year: 2023
aliases:
  - Attention Is All You Need
tags:
  - machine_learning
---
# Attention Is All You Need

>[!summary]
>In this paper, Vaswani et al. introduce the [[transformer|Transformer]], a novel architecture which purely relies on [[attention|attention]] for sequence transduction tasks. In comparison to previous work, the use of attention allows for connections to be made between elements at a further distance, as this mechanism does not rely on sequential processing unlike a recurrent neural network (RNN). 

## Notes

- Transformers are *solely* based on attention and eliminate the need for convolutions or recurrence.
- Transformers are sequence transduction model - aka sequence to sequence modelling
    - encode to a numerical vector
    - decode to an output sequence
    - ex. translation
- Attention has been historically used with RNNs
- Attention allows for dependency modelling without being impacted by the distance in the sequence. 
    - With RNNs the sequential nature adds layers in between each element, which can lead to difficulties making connections between distant elements 
    - e.g. start and end of a long sentence
- Model is auto-regressive, as with previous work
    - The outputs are inputs for the next symbol prediction
- Encoder/decoder architecture

# Citation

Vaswani, A., Shazeer, N., Parmar, N., Uszkoreit, J., Jones, L., Gomez, A. N., Kaiser, L., & Polosukhin, I. (2023). _Attention Is All You Need_ (No. arXiv:1706.03762). arXiv. [http://arxiv.org/abs/1706.03762](http://arxiv.org/abs/1706.03762)


