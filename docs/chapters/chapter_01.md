<p style='text-align: justify;'>
Machine learning models analyse experimental biological data by extracting patterns. The extracted patterns can then be used to give biological insights on similar data that were not previously seen by the model. The degree to which a model retains its performance on new data is called generalization power. Building ML models that generalize well is the main challenge of these methodologies, otherwise the trained models cannot be reused. Preprocessing data properly, and using it in a knowledgeable manner is the only way to obtain good generalization.
</p>



??? Note "Further Reading"
	
    State-of-the-art ML models are often capable of memorizing all the variation in training data. Such models when evaluated on data that they were exposed to during training would create the illusion of mastering the task at hand. However, when tested on an independent set of data (termed a test or validation set), the performance would seem less impressive, suggesting low generalization power of the model. To tackle this problem, initial data should be divided randomly into non-overlapping parts. The simplest approach is to have independent training and testing sets (and possibly a third validation set). Alternatively, the cross-validation or bootstrapping techniques that choose a new training/testing split multiple times from the available data are often considered a preferred solution.

	Overlap of training/testing data splits is particularly troublesome to overcome in biology. For example, in predictions on entire gene and protein sequences, independence of training and testing could be achieved by reducing the number of homologs in the data. Modeling enhancer–promoter contacts requires a different criterion, for example, not sharing one endpoint. Modeling protein domains might require the multidomain sequence to be split into its constituent domains before homology reduction. In short, each area of biology has its own recommendations for handling overlapping data issues, and previous literature is vital to putting forward a strategy.

	Reporting statistics on the dataset size and distribution of data types can help show whether there is a good domain representation in all sets. Simple plots and/or tables showing the number of classes (classification), a histogram of real values binned (regression) and the different types of biological molecules in the data are vital pieces of information for each set. Further, in classification, inclusion of methods that address imbalanced classes is also needed if the class frequencies show as much. Models trained on one dataset may not be successful in dealing with data coming from adjacent but not identical datasets, a phenomenon known as covariance shift. The scale of this effect has been demonstrated in several recent publications—for example, for prediction of disease risk from exome sequencing. Although covariance shift remains an open problem, several potential solutions have been proposed in the area of transfer learning. Moreover, the problem of training ML models that can generalize well on small training data usually requires special models and algorithms.

	Lastly, it is important to make as much data available to the public as possible. Having open access to the data used for experiments, including precise data splits, would ensure better reproducibility of published research and as a result will improve the overall quality of published ML papers. If datasets are not readily available in public repositories, authors should be encouraged to find the most appropriate vehicle—for example, ELIXIR deposition databases or Zenodo—to guarantee the long-term availability of such data.[@DOME]
	

## 1.1 Provenance

- What is the __source__ of the data (database, publication, direct experiment)? 

- If data are in __classes__, how many data points are available in each class—for example, total for the positive (*Npos*) and negative (*Nneg*) cases? 

- If __regression__, how many real value points are there? 

- Has the dataset been __previously used__ by other papers and/or is it recognized by the community?


## 1.2 Dataset Splits

<p style='text-align: justify;'>
How many data points are in the training and test sets? Was a separate validation set used, and if yes, how large was it? Are the distributions of data types in the training and test sets different? Are the distributions of data types in both training and test sets plotted?</p>

## 1.3 Redundancy between data splits

<p style='text-align: justify;'>
 How were the sets split? Are the training and test sets independent? How was this enforced (for example, redundancy reduction to less than X% pairwise identity)? How does the distribution compare to previously published ML datasets?
 </p>

## 1.4 Availability of data

<p style='text-align: justify;'>
Are the data, including the data splits used, released in a public forum? If yes, where (for example, supporting material, URL) and how (license)?
</p>



## 1.5 Example

Here's an example of how the DOME corresponding section would be filled for this publication [@MobiDB] :

|      |        |      |
|-------    |-------    |---------  |
| Data    | Provenance     				    | Protein Data Bank (PDB). X-ray structures missing residues. <br>  Npos = 339,603 residues. <br>  Nneg = 6,168,717 residues. Previously used in (Walsh et al., Bioinformatics 2015) as an independent benchmark set.   |
|     	  | Dataset splits    				    | training set: N/A <br>  Npos,test = 339,603 residues. <br>  Nneg,test = 6,168,717 residues. No validation set. 5.22% positives on the test set.|
|     	  | Redundancy between data splits     | Not applicable.  |
|     	  | Availability of data    		    | Yes, URL: http://protein.bio.unipd.it/mobidblite/. Free use license.|

<br> 

## From Template



!!! example "Exercise"
    This is a question

    ??? success "Solution"
        this is the soluiton to the question