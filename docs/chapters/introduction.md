## The need for standardization

With the significant drop in the cost of many high-throughput technologies, vast amounts of biological data are being generated and made available to researchers. 
Machine learning (ML) has emerged as a powerful tool for analyzing data related to cellular processes, genomics, proteomics, post-translational modifications, metabolism, and drug discovery, offering the potential for transformative medical advancements. 
This trend is evident in the growing number of ML publications, showcasing a wide array of modeling techniques in biology. 
However, although ML methods should ideally be experimentally validated, this occurs in only a small portion of the studies. 
We believe the time is right for the ML community to establish standards for reporting ML-based analyses to facilitate critical evaluation and enhance reproducibility.[@DOME]


<figure>
<img src="../../assets/images/ML_Biology.png" width="600" alt="Bar plots showing the trend of usage of ML in Biology."/>
<figcaption> <p style='text-align: justify;'>The number of ML publications per year is based on Web of Science from 1996 onwards using the topic category for “machine learning” in combination with each of the following terms: “biolog*”, “medicine”, “genom*”, “prote*”, “cell*”, “post translational”, “metabolic” and “clinical”. [@DOME]</p></figcaption>
</figure>


Guidelines or recommendations on the proper construction of machine learning (ML) algorithms can help ensure accurate results and predictions. 
In biomedical research, various communities have established standard guidelines and best practices for managing scientific data and ensuring the reproducibility of computational tools. 
Similarly, within the ML community, there is a growing need for a unified set of recommendations that address data handling, optimization techniques, model development, and evaluation protocols comprehensively.

A recent commentary emphasized the need for standards in ML,suggesting that introducing submission checklists could be a first step toward improving publication practices. 
In response,  a community-driven consensus list of minimal requirements was proposed, framed as questions for ML implementers. By adhering to these guidelines, the quality and reliability of reported methods can be more accurately assessed. 
Our focus is on data, optimization, model, and evaluation (DOME), as these four components encompass the core aspects of most ML implementations. These recommendations are primarily aimed at supervised learning in biological applications where direct experimental validation is absent, as this is the most commonly used ML approach. 
We do not address the use of ML in clinical settings, and it remains to be seen whether the DOME recommendations can be applied to other areas of ML, such as unsupervised, semi-supervised, or reinforcement learning.

## Development of the recommendations


| __Broad topic__     | __Be on the lookout for__       | 	__Consequences__     | __Recommendation(s)__		|
|-------    |-------    |---------  | --------- |
| Data     		| • Inadequate data size & quality <br> • Inappropriate partitioning, dependence between train and test data <br> • Class imbalance <br> • No access to data <br>   | • Data not representative of domain application <br> • Unreliable or biased performance evaluation <br> • Cannot check data credibility   | __• Use independent optimization (training) and evaluation (testing) sets__. This is especially important for meta algorithms, where independence of multiple training sets must be shown to be independent of the evaluation (testing) sets. <br> __• Release data, preferably using appropriate long-term repositories, and include exact splits.__  <br> • Offer sufficient evidence of data size & distribution being representative of the domain.|
| Optimization  | • Overfitting, underfitting, and illegal parameter tuning <br> • Imprecise parameters and protocols given <br>  | • Reported performance is too optimistic or too pessimistic <br> • The model models noise or misses relevant relationships <br> • Results are not reproducible | __• Clarify that evaluation sets were not used for feature selection.__ <br> __• Report indicators on training and testing data that can aid in assessing the possibility of under- or overfitting; for example, train vs. test error.__ <br> __• Release definitions of all algorithmic hyperparameters, regularization protocols, parameters and optimization protocol.__ <br> • For neural networks, release definitions of training and learning curves.  <br>  • Include explicit model validation techniques like *N*-fold cross-validation. |
| Model     	| • Unclear if black box or interpretable model <br> • No access to resulting source code, trained models & data <br> • Execution time impractical | • An interpretable model shows no explainable behavior <br> • Cannot cross compare methods & reproducibility, or check data credibility <br> • Model takes too much time to produce results | __• Describe the choice of black box or interpretable model. If interpretable, show examples of interpretable output.__ <br> • Release documented source code + models + software containers. <br> • Report execution time averaged across repeats. If computationally tough, compare to similar methods. |
| Evaluation    | • Performance measures inadequate <br> • No comparisons to baselines or other methods <br> • Highly variable performance | • Biased performance measures reported <br> • The method is falsely claimed as state-of-the-art <br> • Unpredictable performance in production | __• Compare with public methods & simple models (baselines).__ <br> __• Adopt community-validated measures and benchmark datasets for evaluation.__ <br> • Compare related methods and alternatives on the same dataset.  <br> • Evaluate performance on a final independent held-out set.  <br> __• Use confidence intervals/error intervals and statistical tests to gauge robustness.__ |


The recommendations mentioned above were initially developed by the [ELIXIR Machine Learning Focus Group](https://elixir-europe.org/focus-groups/machine-learning) in response to a published Comment advocating for the establishment of standards in ML for biology. 
This focus group, comprising over 50 experts in the field of ML, held meetings to collaboratively develop and refine the recommendations through broad consensus.




