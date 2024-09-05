<p style='text-align: justify;'>
Optimization, also known as model training, refers to the process of changing values that constitute the model (parameters and hyper-parameters of the model) in a way that maximizes the model’s ability to solve a given problem. In this section, we will focus on problems associated with a poor choice of optimization strategy. 
</p>

??? Note "Further Reading"
	Optimization, also known as training, refers to the process of changing values that constitute the model (parameters and hyperparameters), including preprocessing steps, in a way that maximizes the model’s ability to solve a given problem. A poor choice of optimization strategy may lead to issues such as over- or underfitting.
	A model that has suffered severe overfitting will show an excellent performance on training data while performing poorly on unseen data, rendering it useless for real-life applications. On the other side of the spectrum, underfitting occurs when very simple models capable of capturing only straightforward dependencies between features are applied to data of a more complex nature. 
	Algorithms for feature selection32 can be employed to reduce the chances of overfitting. However, feature selection and other preprocessing actions come with their own recommendations. The main one is to abstain from using non-training data for feature selection and preprocessing—a particularly hard issue to spot for meta-predictors, which may lead to an overestimation of performance.

	Finally, the release of files showing the exact specification of the optimization protocol and the type of parameters or hyperparameters are a vital characteristic of the final algorithm. Lack of documentation, including limited accessibility to relevant records for the parameters, hyperparameters and optimization protocol, may further compound the understanding of the overall model performance.[@DOME]


## 2.1 Algorithm

- __What__ is the ML algorithm class used? 
- Is the ML algorithm __new__? 
- If yes, why was it __chosen__ over better known alternatives?

## 2.2 Meta-predictions

- Does the model use data from __other__ ML algorithms as input? 
- If yes, which ones? 
- Is it clear that training data of initial predictors and meta-predictor are __independent__ of test data for the meta-predictor?

## 2.3 Data encoding

- How were the data __encoded__ and __preprocessed__ for the ML algorithm?

## 2.4 Parameters

- How many __parameters__ (*p*) are used in the model? 
- How was p selected?

## 2.5 Features

- How many __features__ (*f*) are used as input? 
- Was __feature selection__ performed? 
- If yes, was it performed using the __training set only__?

## 2.6 Fitting

- Is *p* much larger than the number of training points and/or is *f* large (for example, in classification is *p >> (Npos + Nneg)*and/or *f > 100*)? 
- If yes, how was __overfitting__ ruled out? 
- Conversely, if the number of training points is much larger than *p* and/or *f* is small (for example, *(Npos + Nneg) >> p*  and/or *f < 5*), how was __underfitting__ ruled out?

## 2.7 Regularization

- Were any __overfitting prevention techniques__ used (for example, early stopping using a validation set)? 
-If yes, __which__ ones?

## 2.8 Availability of configuration
- Are the hyperparameter configurations, optimization schedule, model files and optimization parameters reported? 
- If yes, where (for example, URL) and how (license)?