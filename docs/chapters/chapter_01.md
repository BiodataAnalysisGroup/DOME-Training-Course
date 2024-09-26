<p style='text-align: justify;'>
ML models analyze experimental biological data by identifying patterns, which can then be used to generate biological insights from similar, previously unseen data. 
The ability of a model to maintain its performance on new data is referred to as its generalization power. 
Achieving strong generalization is a key challenge in developing ML models; without it, trained models cannot be effectively reused. 
Properly preprocessing data and using it in an informed way are essential steps to ensure good generalization.
</p>



??? Note "Further Reading"
	
    State-of-the-art ML models are often capable of memorizing all variations within the training data. As a result, when evaluated on data from the training set, they may give the false impression of excelling at the given task. However, their performance tends to diminish when tested on independent data (called the test or validation set), revealing a lower generalization power. To address this issue, the original dataset should be randomly split into non-overlapping parts. The simplest method involves creating separate training and test sets (with a possible third validation set). Alternatively, more robust techniques like cross-validation or bootstrapping, which repeatedly create different training/testing splits from the available data, are often preferred.
	
	Handling overlap between training and test data can be especially challenging in biology. For instance, in predicting entire gene or protein sequences, ensuring data independence might require reducing homologs in the dataset. In modeling enhancer–promoter contacts, a different criterion may be needed, such as ensuring that no endpoint is shared between training and test sets. Similarly, modeling protein domains may require splitting multidomain sequences into their individual domains before applying homology reduction. Each biological field has its own methods for managing overlapping data, making it crucial to consult prior literature when developing an approach.
	
	Providing details on the size of the dataset and the distribution of data types helps demonstrate whether the data is well-represented across different sets. Simple visualizations, such as plots or tables, showing the number of classes (for classification), a histogram of binned values (for regression), and the various types of biological molecules included in the data, are essential for understanding each set. Additionally, for classification tasks, methods that account for imbalanced classes should be used if the class frequencies suggest a significant imbalance.
	
	It’s also important to note that models trained on one dataset may not perform well on closely related, but distinct, datasets—a phenomenon known as "covariance shift." This issue has been observed in several recent studies, such as those predicting disease risk from exome sequencing data. While covariance shift remains an open problem, potential solutions have been proposed, particularly in the field of transfer learning. Furthermore, building ML models that generalize well on small training datasets often requires specialized models and algorithms.
	
	Finally, making experimental data publicly available is crucial. Open access to datasets, including precise data splits, enhances the reproducibility of research and improves the overall quality of ML publications. If public repositories are not available, authors should be encouraged to use platforms like ELIXIR deposition databases or Zenodo to ensure long-term data accessibility.[@DOME]
	

## 1.1 Provenance 

<p style='text-align: justify;'>
Provenance of data refers to the origin, history, and lineage of data—essentially, tracking where the data came from, how it has been processed, and how it has moved through various systems. It’s like a detailed record that traces the data's life cycle from creation to its current state. Understanding data provenance helps ensure transparency, trustworthiness, and reliability in data usage.
</p>

<ins>Key Questions</ins>

- What is the __source__ of the data (database, publication, direct experiment)? 
- If data are in __classes__, how many data points are available in each class—for example, total for the positive (*Npos*) and negative (*Nneg*) cases? 
- If __regression__, how many real value points are there? 
- Has the dataset been __previously used__ by other papers and/or is it recognized by the community?

!!! example "From Example Publication"
	
	Protein Data Bank (PDB). X-ray structures missing residues. <br>  *Npos* = 339,603 residues. <br>  *Nneg* = 6,168,717 residues. <br> Previously used in (Walsh et al., Bioinformatics 2015) as an independent benchmark set.


## 1.2 Dataset Splits

<p style='text-align: justify;'>
Dataset splits refer to the process of dividing a dataset into distinct subsets for different purposes, mainly in machine learning or data science tasks. The most common splits are:
</p>

- Training Set: This is the largest subset, used to train the machine learning model. The model "learns" from this data by adjusting its internal parameters to minimize prediction errors.

- Validation Set: A separate subset used to fine-tune the model's hyperparameters. The model doesn't learn directly from this data, but it helps monitor the model's performance and avoid overfitting, which is when a model becomes too tailored to the training data and doesn't generalize well.

- Test Set: This is the final subset, used to evaluate the model's performance. The test set remains unseen by the model until after training and validation are complete, providing an unbiased estimate of how well the model generalizes to new, unseen data.


<p style='text-align: justify;'>
In addition to these, there are some variations in dataset splitting strategies:
</p>


- Holdout Split: A simple division where a fixed percentage of data is reserved for testing (e.g., 80% training, 20% test).

- Cross-validation: In this technique, the dataset is split multiple times into training and validation sets, ensuring each data point is used for validation at least once (e.g., 5-fold cross-validation). This provides a more robust evaluation of the model’s performance.


<ins>Key Questions</ins>

- How __many data points__ are in the training and test sets? 
- Was a __separate validation__ set used, and if yes, how large was it? 
- Are the __distributions__ of data types (*N<sub>pos</sub>* and *N<sub>neg</sub>*) in the training and test sets different? Are the distributions of data types in both training and test sets plotted?

!!! example "From Example Publication"
	Protein Data Bank (PDB). X-ray structures missing residues. <br>  *Npos* = 339,603 residues. <br>  *Nneg* = 6,168,717 residues. <br> Previously used in (Walsh et al., Bioinformatics 2015) as an independent benchmark set.


## 1.3 Redundancy between data splits

<p style='text-align: justify;'>
 Redundancy between data splits occurs when the same data points are present in more than one of the training, validation, or test sets. This is undesirable because it can distort model evaluation and lead to overoptimistic performance metrics (e.g. eliminating data points more similar than X%). 
This may effect the mfodel by introcuding an overfitting risk, unreliable performance metrics and/or lack of generalization.
</p>

<ins>Key Questions</ins>

 - How were the sets __split__? 
 - Are the training and test sets __independent__? 
 - How was this __enforced__ (for example, redundancy reduction to less than X% pairwise identity)? 
 - How does the distribution compare to __previously published__ ML datasets?

!!! example "From Example Publication"
	Not applicable.  

## 1.4 Availability of data

<p style='text-align: justify;'>
Availability of data refers to the accessibility and readiness of data for use in various applications, such as analysis, machine learning, decision-making, or reporting. It ensures that data can be retrieved and utilized when needed by users or systems.
</p>


<ins>Key Questions</ins>

- Are the data, including the data splits used, __released__ in a public forum? 
- If yes, __where__ (for example, supporting material, URL) and __how__ (license)?

!!! example "From Example Publication"
	Yes, URL: http://protein.bio.unipd.it/mobidblite/. <br> Free use license.

<br> 
