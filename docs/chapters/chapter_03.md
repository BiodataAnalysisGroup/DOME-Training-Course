<p style='text-align: justify;'>
Good overall performance and the model's ability to generalize well to unseen data are crucial factors that significantly impact the applicability of any proposed ML research. However, several other important aspects related to ML models must also be considered.
</p>

??? Note "Further Reading"
	Equally important aspects of ML models include their interpretability and reproducibility. Interpretable models can identify causal relationships in the data and provide logical explanations for their predictions, which is especially valuable in fields like drug design and diagnostics. In contrast, black box models, while often accurate, may not offer understandable insights into the reasons behind their predictions. Both types of models are discussed in more detail elsewhere, and choosing between them involves weighing their respective benefits. The key recommendation is to clearly state whether the model is a black box or interpretable, and if it is interpretable, to provide clear examples of its outputs.
	
	Reproducibility is crucial for ensuring that research outcomes can be effectively utilized and validated by the broader community. Challenges with model reproducibility go beyond merely documenting parameters, hyperparameters, and optimization protocols. Limited access to essential model components (such as source code, model files, parameter configurations, and executables) and high computational demands for running trained models on new data can severely restrict or even prevent reproducibility.[@DOME]


## 3.1 Interpretability

<p style='text-align: justify;'>
Model interpretability refers to the extent to which a human can understand the decisions and predictions made by a ML model. 
Interpretability is crucial for building trust in model outcomes, especially in high-stakes domains such as healthcare and finance, where understanding the rationale behind a model's predictions can have significant implications.
For example neural networks are often criticized for being "black boxes," as their internal workings (like hidden layers) are less transparent, making them more difficult to trust.
There are generally two types of interpretability:
</p>

- <p style='text-align: justify;'> Global Interpretability refers to the ability to understand the overall behavior of the model across all predictions. It involves explaining how the model works as a whole and what features are important in determining predictions. </p>

- <p style='text-align: justify;'> Local interpretability focuses on understanding individual predictions made by the model. It aims to explain why a specific input led to a particular output. </p>

<ins>Key Questions</ins>

- Is the model __black box__ or __interpretable__? 
- If the model is interpretable, can you give clear __examples__ of this?

!!! example "From Example Publication"
	Transparent, in so far as meta-prediction is concerned. Consensus and post processing over other methods predictions (which are mostly black boxes). No attempt was made to make the meta-prediction a black box.


## 3.2 Output

<p style='text-align: justify;'>
The output of a machine learning model refers to the predictions or classifications made by the model after processing input data. 
Depending on the type of model and the nature of the problem, the output can vary widely. 
Here’s a breakdown of some different types of outputs: 
</p>

- <p style='text-align: justify;'> __Regression__ includes continuous values that estimates a quantity based on the input features </p>

- <p style='text-align: justify;'> In __classification__ tasks the output is a category or class label that indicates which class the input belongs to. </p>

- <p style='text-align: justify;'> In __multi-class classification__ the model predicts one class from multiple possible classes. </p>

- <p style='text-align: justify;'> __Multi-label classification__ includes the assignment of multiple classes to a single input.</p>

<ins>Key Questions</ins>

- Is the model __classification__ or __regression__?

!!! example "From Example Publication"
	Classification, i.e. residues thought to be disordered.

## 3.3 Execution time

<p style='text-align: justify;'>
Execution time in the context of ML refers to the duration it takes for a model to perform a specific task, such as training, predicting, or evaluating performance. 
Understanding and measuring execution time is crucial for various reasons, including optimizing model performance, resource management, and user experience. 
</p>

CPU time of single representative execution on standard hardware (e.g. seconds on desktop PC).

<ins>Key Questions</ins>

-  How much __time__ does a single representative prediction require on a standard machine (for example, seconds on a desktop PC or high-performance computing cluster)?

!!! example "From Example Publication"
	ca. 1 second per representative on a desktop PC.

## 3.4 Availability of software

<p style='text-align: justify;'>
Availability of software refers to the accessibility, reliability, and usability of various software tools and libraries that facilitate the development, training, deployment, and evaluation of ML models. 
This includes both open-source and proprietary software, and it is critical for researchers and practitioners to have the right tools at their disposal to effectively work on tasks.
</p>

<ins>Key Questions</ins>

- Is the __source code__ released? 
- Is a __method to run__ the algorithm (executable, web server, virtual machine or container instance) released? 
- If yes, __where__ (for example github, zenodo or other repository URL) and __how__ (for example MIT license)?

!!! example "From Example Publication"
	Yes, URL: http://protein.bio.unipd.it/mobidblite/. <br>  Bespoke license free for academic use

<br> 