# Normalization

## Why does normalization work?
The way normalization used in deep models are making training more stable and faster while using wider range of learning rate.
<p align="center">
<img width="596" alt="Screenshot 2023-08-28 at 11 15 18" src="https://github.com/Amir-P/ml_questions/assets/8766492/78a7a6fa-9cb5-48c5-8cbb-5fcd7b0f4b6c">
</p>
Reading about it, I found some resources including the original paper believing that benefits of normalization comes from the reduce in ICS (Internal Covariate Shift). According to (Santurkar et al.)[https://papers.nips.cc/paper/2018/file/905056c1ac1dad141560467e0a99e1cf-Paper.pdf] that's not the case. In fact sometimes normalization causes ICS to get worst.
<p align="center">
<img width="737" alt="Screenshot 2023-08-28 at 11 16 03" src="https://github.com/Amir-P/ml_questions/assets/8766492/4e17f2a3-e6f2-4439-b355-c4a64af81f8f">
<img width="874" alt="Screenshot 2023-08-28 at 11 16 58" src="https://github.com/Amir-P/ml_questions/assets/8766492/ef22ea7f-0d6f-4e6d-9340-7e46bed7b6de">
</p>

They found that normalizing benefits training process of models via reparameterizing the optimization problem and smoothing it's landscape thus making gradients become more predictive preventing gradient vanishing/explosion.
<p align="center">
<img width="933" alt="Screenshot 2023-08-28 at 11 16 18" src="https://github.com/Amir-P/ml_questions/assets/8766492/3dc94244-41d5-4a4b-9e22-6f632514f63b">
</p>

## Why is there a linear transformation after normalization in norm layers?
I'm still not convinced by the explanations for this question. (Santurkar et al.)[https://papers.nips.cc/paper/2018/file/905056c1ac1dad141560467e0a99e1cf-Paper.pdf] says that applying this transformation retains model expressivity.
