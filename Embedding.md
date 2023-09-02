# Embedding

## What is weight tying?
Weight tying proposed by [Press et al.](https://arxiv.org/abs/1608.05859v3) is a technique for reducing number of parameters in sequence to sequence models by using the same weights for output embedding as the input embedding when we have the same vocab for input and output. The transformer model implementation from HuggingFace scales the outputs before passing to the output embedding by `sqrt(d_model)`.