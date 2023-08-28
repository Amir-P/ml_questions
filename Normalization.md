# Normalization

## Why does normalization work?
The way normalization used in deep models are making training more stable and faster while using wider range of learning rate.
<p align="center">
<img width="592" alt="Screenshot 2023-08-28 at 11 04 31" src="https://github.com/Amir-P/ml_questions/assets/8766492/1ca65fb6-c279-4b9b-902a-6590fe6378b2">
</p>
Reading about it, I found some resources including the original paper believing that benefits of normalization comes from the reduce in ICS (Internal Covariate Shift). According to (Santurkar et al.)[https://papers.nips.cc/paper/2018/file/905056c1ac1dad141560467e0a99e1cf-Paper.pdf] that's not the case. In fact sometimes normalization causes ICS to get worst.
<p align="center">
<img width="724" alt="Screenshot 2023-08-28 at 11 02 24" src="https://github.com/Amir-P/ml_questions/assets/8766492/3f5edfa1-9821-44ac-b878-e8f0d017050d">
<img width="881" alt="Screenshot 2023-08-28 at 11 02 54" src="https://github.com/Amir-P/ml_questions/assets/8766492/dba817b0-9938-41b8-b8bf-6fe6f7642ee8">
</p>

They found that normalizing benefits training process of models via reparameterizing the optimization problem and smoothing it's landscape thus making gradients become more predictive preventing gradient vanishing/explosion.
<p align="center">
<img width="928" alt="Screenshot 2023-08-28 at 11 03 12" src="https://github.com/Amir-P/ml_questions/assets/8766492/d9c27aa8-0d59-46e9-be53-e48b59d6d33a">
</p>

## Why is there a linear transformation after normalization in norm layers?
I'm still not convinced by the explanations for this question. (Santurkar et al.)[https://papers.nips.cc/paper/2018/file/905056c1ac1dad141560467e0a99e1cf-Paper.pdf] says that applying this transformation retains model expressivity.
