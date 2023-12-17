# Adapting-Linear-Attention-to-Query-Key-Distributions

I adapt the complex exponential estimator (CEXP), first introduced in [Choroman-
ski et al. (2022)](https://arxiv.org/abs/2110.04367), to the setting where query and key vectors are assumed to be
sampled from two different multivariate normal distributions. I find that many of
the strong theoretical results derived in Choromanski et al. (2022) and [Choroman-
ski et al. (2021)](https://arxiv.org/abs/2009.14794) apply to CEXP due to the similarities between the CEXP and
PRF softmax kernel estimators, and I use these to obtain concentration results that
take the query and key distributions into account. I also derive a simple heuristic
for choosing the parameters of the CEXP estimator and empirically demonstrate
that this new method leads to improved mean squared error and max relative error
results.

## Empirical Results

Below is a boxplot demonstrating the effectiveness of my heuristic for choosing HCEXP estimator parameters (right column of graph):

<img src="https://github.com/jblackwelder64/Adapting-Linear-Attention-to-Query-Key-Distributions/blob/main/download%20(2).png">

Scatter plot comparing HCEXP estimator predictions (using my heuristic) with true softmax kernel values:

<img src="Sample Predictions/Plate_ePB_v1_bulk_20220704_WellB4_ChannelDAPI,DsRed,Cy5_Seq0007 - Denoised.nd2fov_1.tif_PRED_INSTANCE_MASK.png">

Scatter plot comparing HCEXP estimator predictions (not using my heuristic) with true softmax kernel values:

<img src="https://github.com/jblackwelder64/Adapting-Linear-Attention-to-Query-Key-Distributions/blob/main/download%20(1).png">