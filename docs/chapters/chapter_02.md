<p style='text-align: justify;'>
Optimization, or model training, refers to the process of adjusting the values that make up the model (including both parameters and hyperparameters) to enhance the model's performance in solving a given problem. In this section, we will focus on challenges that arise from selecting suboptimal optimization strategies.</p>

??? Note "Further Reading"
	Optimization, or training, involves adjusting the values that define a model (such as parameters and hyperparameters), as well as preprocessing steps, to enhance the model’s ability to solve a given problem. Choosing an inappropriate optimization strategy can lead to issues like overfitting or underfitting.
	
	Overfitting occurs when a model performs exceptionally well on training data but fails on unseen data, making it ineffective in real-world scenarios. Underfitting, on the other hand, happens when overly simplistic models, capable of capturing only basic relationships between features, are applied to more complex data.
	
	Feature selection algorithms can help reduce the risk of overfitting, but they come with their own set of guidelines. A key recommendation is to avoid using non-training data for feature selection and preprocessing. This is especially problematic for meta-predictors, as it can lead to an overestimation of the model’s performance.
	
	Finally, making files that detail the exact optimization protocol, including parameters and hyperparameters, publicly available is crucial. A lack of proper documentation and limited access to these records can hinder the understanding and evaluation of the model’s overall performance.[@DOME]


## 2.1 Algorithm

- __What__ is the ML algorithm class used? 
- Is the ML algorithm __new__? 
- If yes, why was it __chosen__ over better known alternatives?

|    Algorithm Section Example  |
|---------  |
| Majority-based consensus classification based on 8 primary ML methods and post-processing. |


## 2.2 Meta-predictions

- Does the model use data from __other__ ML algorithms as input? 
- If yes, which ones? 
- Is it clear that training data of initial predictors and meta-predictor are __independent__ of test data for the meta-predictor?

|    Meta-predictions Section Example  |
|---------  |
| Yes, predictor output is a binary prediction computed from the consensus of other methods; Independence of training sets of other methods with test set of meta-predictor was not tested since datasets from other methods were not available. |


## 2.3 Data encoding

- How were the data __encoded__ and __preprocessed__ for the ML algorithm?

|    Data encoding Section Example  |
|---------  |
| Label-wise average of 8 binary predictions. |

## 2.4 Parameters

- How many __parameters__ (*p*) are used in the model? 
- How was p selected?

|    Parameters Section Example  |
|---------  |
| p = 3 (Consensus score threshold, expansion-erosion window, length threshold). <br> No optimization. |

## 2.5 Features

- How many __features__ (*f*) are used as input? 
- Was __feature selection__ performed? 
- If yes, was it performed using the __training set only__?

|    Features Section Example  |
|---------  |
| Not applicable. |

## 2.6 Fitting

- Is *p* much larger than the number of training points and/or is *f* large (for example, in classification is *p >> (Npos + Nneg)*and/or *f > 100*)? 
- If yes, how was __overfitting__ ruled out? 
- Conversely, if the number of training points is much larger than *p* and/or *f* is small (for example, *(Npos + Nneg) >> p*  and/or *f < 5*), how was __underfitting__ ruled out?

|  Fitting Section Example  |
|---------  |
| Single input ML methods are used with default parameters. <br> Optimization is a simple majority. |

## 2.7 Regularization

- Were any __overfitting prevention techniques__ used (for example, early stopping using a validation set)? 
-If yes, __which__ ones?

|  Regularization Section Example  |
|---------  |
| No. |


## 2.8 Availability of configuration
- Are the hyperparameter configurations, optimization schedule, model files and optimization parameters reported? 
- If yes, where (for example, URL) and how (license)?

|  Availability of configuration Section Example  |
|---------  |
|  Not applicable.|


<br> 