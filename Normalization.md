# Normalization

## Why does normalization work?
The way normalization used in deep models are making training more stable and faster while using wider range of learning rate.
Reading about it, I found some resources including the original paper believing that benefits of normalization comes from the reduce in ICS (Internal Covariate Shift). According to (Santurkar et al.)[https://papers.nips.cc/paper/2018/file/905056c1ac1dad141560467e0a99e1cf-Paper.pdf] that's not the case. In fact sometimes normalization causes ICS to get worth.

They found that normalizing benefits training process of models via reparameterizing the optimization problem and smoothing it's landscape thus making gradients become more predictive preventing gradient vanishing/explosion.

## Why is there a linear transformation after normalization in norm layers?
I'm still not convinced by the explanations for this question. (Santurkar et al.)[https://papers.nips.cc/paper/2018/file/905056c1ac1dad141560467e0a99e1cf-Paper.pdf] says that applying this transformation retains model expressivity.