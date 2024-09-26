<p style='text-align: justify;'>
Optimization, or model training, refers to the process of adjusting the values that make up the model (including both parameters and hyperparameters) to enhance the model's performance in solving a given problem. In this section, we will focus on challenges that arise from selecting suboptimal optimization strategies.
</p>

??? Note "Further Reading"
	Optimization, or training, involves adjusting the values that define a model (such as parameters and hyperparameters), as well as preprocessing steps, to enhance the model’s ability to solve a given problem. Choosing an inappropriate optimization strategy can lead to issues like overfitting or underfitting.
	
	Overfitting occurs when a model performs exceptionally well on training data but fails on unseen data, making it ineffective in real-world scenarios. Underfitting, on the other hand, happens when overly simplistic models, capable of capturing only basic relationships between features, are applied to more complex data.
	
	Feature selection algorithms can help reduce the risk of overfitting, but they come with their own set of guidelines. A key recommendation is to avoid using non-training data for feature selection and preprocessing. This is especially problematic for meta-predictors, as it can lead to an overestimation of the model’s performance.
	
	Finally, making files that detail the exact optimization protocol, including parameters and hyperparameters, publicly available is crucial. A lack of proper documentation and limited access to these records can hinder the understanding and evaluation of the model’s overall performance.[@DOME]


## 2.1 Algorithm

<p style='text-align: justify;'>
Since algorithms take input data and produce output, typically solving a particular problem or achieving a specific objective, it is essential to know which one is implemented in a study. In this way we can have better insights for the results of learning patterns, relationships, or rules that can then be applied to new, unseen data.
Regarding ML class there are three major categories:
</p>

- Supervised (i.e. Linear Regression, Logistic Regression, Decision Trees, Support Vector Machines (SVM) and others), 
- Unsupervised Learning (i.e. K-Means Clustering, Principal Component Analysis (PCA) and Hierarchical Clustering and others),  
- Reinforcement Learning (i.e. Q-Learning, Deep Q-Networks (DQN) and others). (e.g. neural network, random forest, SVM). 


<ins>Key Questions</ins>

- __What__ is the ML algorithm class used? 
- Is the ML algorithm __new__? 
- If yes, why was it __chosen__ over better known alternatives?

!!! example "From Example Publication"
	Majority-based consensus classification based on 8 primary ML methods and post-processing.


## 2.2 Meta-predictions

<p style='text-align: justify;'>
Meta-predictions refer to predictions made by models that aggregate or utilize the outputs (predictions) of other models. Essentially, meta-prediction systems combine predictions from multiple models to produce a more robust or accurate final prediction. Meta-predictions are often used in ensemble learning techniques, where the goal is to leverage the strengths of several models to enhance overall performance.
</p>


<ins>Key Questions</ins>

- Does the model use data from __other__ ML algorithms as input? 
- If yes, which ones? 
- Is it clear that training data of initial predictors and meta-predictor are __independent__ of test data for the meta-predictor?

!!! example "From Example Publication"
	Yes, predictor output is a binary prediction computed from the consensus of other methods; Independence of training sets of other methods with test set of meta-predictor was not tested since datasets from other methods were not available.


## 2.3 Data encoding

<p style='text-align: justify;'>
Data encoding is the process of transforming data from one format or structure into another, often to make it easier for ML models or computational systems to process. 
In ML, data often needs to be encoded to ensure that it can be effectively interpreted by algorithms, especially for algorithms that require numerical input (e.g., neural networks, SVMs).
</p>

<ins>Key Questions</ins>

- How were the data __encoded__ and __preprocessed__ for the ML algorithm?

!!! example "From Example Publication"
	Label-wise average of 8 binary predictions.

## 2.4 Parameters

<p style='text-align: justify;'>
Model parameters are the internal configurations or variables that a model learns from the training data. 
These parameters determine how the model makes predictions and how well it fits the training data. 
The values of these parameters are adjusted during the training process through algorithms like gradient descent or optimization procedures. 
</p>

<ins>Key Questions</ins>

- How many __parameters__ (*p*) are used in the model? 
- How were *p* selected?

!!! example "From Example Publication"
	p = 3 (Consensus score threshold, expansion-erosion window, length threshold). <br> No optimization.

## 2.5 Features

<p style='text-align: justify;'>
In the context of ML, features refer to the individual measurable properties or characteristics of the data being used for training a model. 
They play a crucial role in determining the performance of ML models, as they provide the information that the model needs to make predictions or classifications.
Feature Engineering is the process of creating, modifying, or selecting the most relevant features from the raw data to improve model performance by reducing model complexity, improving training time and avoiding overfitting. 
</p>

<ins>Key Questions</ins>

- How many __features__ (*f*) are used as input? 
- Was __feature selection__ performed? 
- If yes, was it performed using the __training set only__?

!!! example "From Example Publication"
	Not applicable.

## 2.6 Fitting

<p style='text-align: justify;'>
Fitting refers to the process of training a ML model on a dataset by adjusting its parameters to minimize prediction error. 
The goal is to find a balance between underfitting and overfitting, ensuring that the model captures the underlying patterns in the data while still generalizing well to unseen data. 
Proper evaluation, regularization, and tuning of the model during the fitting process are crucial to achieving a good fit.
</p>

<ins>Key Questions</ins>

- Is *p* much larger than the number of training points and/or is *f* large (for example, in classification is *p >> (N<sub>pos</sub> + N<sub>neg</sub>)* and/or *f > 100*)? 
- If yes, how was __overfitting__ ruled out? 
- Conversely, if the number of training points is much larger than *p* and/or *f* is small (for example, *(N<sub>pos</sub> + N<sub>neg</sub>) >> p*  and/or *f < 5*), how was __underfitting__ ruled out?

!!! example "From Example Publication"
	Single input ML methods are used with default parameters. <br> Optimization is a simple majority.

## 2.7 Regularization

<p style='text-align: justify;'>
Regularization is a technique used to prevent overfitting by adding a penalty to the loss function, which discourages the model from becoming too complex. Common regularization techniques include:
</p>

- L1 Regularization (Lasso): Adds a penalty proportional to the absolute value of the coefficients. It encourages sparsity, setting some coefficients to zero.
- L2 Regularization (Ridge): Adds a penalty proportional to the square of the coefficients, discouraging large coefficients and thus reducing model complexity.
- Dropout (in neural networks): Randomly drops a percentage of neurons during training, which helps prevent overfitting by forcing the network to generalize.


<ins>Key Questions</ins>

- Were any __overfitting prevention techniques__ used (for example, early stopping using a validation set)?

- If yes, __which__ ones?

!!! example "From Example Publication"
	No. 


## 2.8 Availability of configuration

<p style='text-align: justify;'>

Availability of configuration refers to the accessibility and transparency of the settings, parameters, and options that can be adjusted or customized in a ML model or system. 
These configurations control how the model is trained, how it makes predictions, and how it operates in different environments. 
Ensuring that the configuration is available, flexible, and easy to modify is important for reproducibility, fine-tuning, and deployment of models.
</p>

<ins>Key Questions</ins>

- Are the hyperparameter configurations, optimization schedule, model files and optimization parameters __reported__? 
- If yes, __where__ (for example, URL) and __how__ (license)?

!!! example "From Example Publication"
	Not applicable.

<br> 