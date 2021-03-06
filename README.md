# Hierarchical Block Distance Model (HBDM)

Python 3.8.3 and Pytorch 1.9.0 implementation of the Hierarchical Block Distance Model (HBDM).

## Description

We propose a novel graph representation learning method named the Hierarchical Block Distance Model (HBDM). It extracts node embeddings imposing a multiscale block-structure that accounts for homophily and transitivity properties across the levels of the inferred hierarchy. Notably, the HBDM naturally accommodates unipartite, directed, and bipartite networks whereas the hierarchy is designed to ensure linearithmic time and space complexity enabling the analysis of very large-scale networks. We evaluate the performance of our approach on massive networks consisting of millions of nodes. Our HBDM framework significantly outperforming recent scalable approaches in downstream tasks providing superior performance even using ultra low-dimensional embeddings at the same time facilitating direct and hierarchical-aware network visualization and interpretation.


### Installation
pip install -r requirements.txt

Our Pytorch implementation heavily relies on the [pytorch_sparse](https://github.com/rusty1s/pytorch_sparse) library. Installation guidelines can be found at the corresponding [Github repository](https://github.com/rusty1s/pytorch_sparse).

### Learning hierarchical and multi-scale graph representations with HBDM
RUN: python main.py

optional arguments:

--epochs  &emsp;  number of epochs for training (default: 15K)

--RH    &emsp;    number of epochs to rebuild the hierarchy from scratch (default: 25)

--cuda  &emsp;    CUDA training (default: True)

--LP   &emsp;     performs link prediction (default: True)

--D   &emsp;      dimensionality of the embeddings (default: 2)

--lr   &emsp;     learning rate for the ADAM optimizer (default: 0.1)

--RE   &emsp;     activates random effects (default: True)

--dataset &emsp;  dataset to apply HBDM' (default: grqc)

### CUDA Implementation

The code has been primarily constructed and optimized for running in a GPU-enabled environment.

### References
A Hierarchical Block Distance Model for Ultra Low-Dimensional Graph Representations, Under Double-Blind Review.

