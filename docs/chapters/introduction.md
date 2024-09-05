## The need for standardization

With the steep decline in the cost of many high-throughput technologies, large amounts of biological data are being generated and made accessible to researchers. 
Machine learning (ML) has come into the spotlight as a very useful approach for understanding cellular, genomic, proteomic, post-translational, metabolic and drug discovery data, with the potential to result in ground-breaking medical applications. 
This is clearly reflected in the corresponding growth of ML publications, reporting a wide range of modeling techniques in biology. 
While ideally ML methods should be validated experimentally, this happens only in a fraction of the publications. 
We believe that the time is right for the ML community to develop standards for reporting ML-based analyses to enable critical assessment and improve reproducibility. [@DOME]


<figure>
<img src="../../assets/images/ML_Biology.png" width="600" alt="Bar plots showing the trend of usage of ML in Biology."/>
<figcaption> <p style='text-align: justify;'>The number of ML publications per year is based on Web of Science from 1996 onwards using the topic category for “machine learning” in combination with each of the following terms: “biolog*”, “medicine”, “genom*”, “prote*”, “cell*”, “post translational”, “metabolic” and “clinical”. </p></figcaption>
</figure>


Guidelines or recommendations on how to appropriately construct ML algorithms can help to ensure correct results and predictions. 
In biomedical research, communities have defined standard guidelines and best practices for scientific data management and reproducibility of computational tools. 
On the ML community side, there is demand for a cohesive and combined set of recommendations with respect to data, the optimization techniques, the final model, and evaluation protocols as a whole.


A recent comment highlighted the need for standards in ML, arguing for the adoption of on-submission checklists as a first step toward improving publication standards. 
Through a community-driven consensus, we propose a list of minimal requirements asked as questions to ML implementers that, if followed, will help to assess the quality and reliability of reported methods more faithfully. 
We have focused on data, optimization, model and evaluation (DOME) as each component of an ML implementation usually falls within one of these four topics.
Our recommendations are made primarily for the case of supervised learning in biological applications in the absence of direct experimental validation, as this is the most common type of ML approach used. 
We do not discuss how ML can be used in clinical applications. It also remains to be determined whether the DOME recommendations can be extended to other fields of ML, like unsupervised, semisupervised and reinforcement learning.

## Development of the recommendations


| __Broad topic__     | __Be on the lookout for__       | 	__Consequences__     | __Recommendation(s)__		|
|-------    |-------    |---------  | --------- |
| Data     		| • Inadequate data size & quality <br> • Inappropriate partitioning, dependence between train and test data <br> • Class imbalance <br> • No access to data <br>   | • Data not representative of domain application <br> • Unreliable or biased performance evaluation <br> • Cannot check data credibility   | __• Use independent optimization (training) and evaluation (testing) sets__. This is especially important for meta algorithms, where independence of multiple training sets must be shown to be independent of the evaluation (testing) sets. <br> __• Release data, preferably using appropriate long-term repositories, and include exact splits.__  <br> • Offer sufficient evidence of data size & distribution being representative of the domain.|
| Optimization  | • Overfitting, underfitting, and illegal parameter tuning <br> • Imprecise parameters and protocols given <br>  | • Reported performance is too optimistic or too pessimistic <br> • The model models noise or misses relevant relationships <br> • Results are not reproducible | __• Clarify that evaluation sets were not used for feature selection.__ <br> __• Report indicators on training and testing data that can aid in assessing the possibility of under- or overfitting; for example, train vs. test error.__ <br> __• Release definitions of all algorithmic hyperparameters, regularization protocols, parameters and optimization protocol.__ <br> • For neural networks, release definitions of training and learning curves.  <br>  • Include explicit model validation techniques like *N*-fold cross-validation. |
| Model     	| • Unclear if black box or interpretable model <br> • No access to resulting source code, trained models & data <br> • Execution time impractical | • An interpretable model shows no explainable behavior <br> • Cannot cross compare methods & reproducibility, or check data credibility <br> • Model takes too much time to produce results | __• Describe the choice of black box or interpretable model. If interpretable, show examples of interpretable output.__ <br> • Release documented source code + models + software containers. <br> • Report execution time averaged across repeats. If computationally tough, compare to similar methods. |
| Evaluation    | • Performance measures inadequate <br> • No comparisons to baselines or other methods <br> • Highly variable performance | • Biased performance measures reported <br> • The method is falsely claimed as state-of-the-art <br> • Unpredictable performance in production | __• Compare with public methods & simple models (baselines).__ <br> __• Adopt community-validated measures and benchmark datasets for evaluation.__ <br> • Compare related methods and alternatives on the same dataset.  <br> • Evaluate performance on a final independent held-out set.  <br> __• Use confidence intervals/error intervals and statistical tests to gauge robustness.__ |


The recommendations outlined above were initially formulated through the [ELIXIR Machine Learning Focus Group](https://elixir-europe.org/focus-groups/machine-learning) after the publication of a Comment calling for the establishment of standards for ML in biology. 
which consists of more than 50 experts int he field of ML and held meetings to develop and refine recommendations based on a broad consensus.




