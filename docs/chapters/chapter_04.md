<p style='text-align: justify;'>
In implementing a robust and trustworthy ML method, providing a comprehensive data description, adhering to a correct optimization protocol, and ensuring that the model is clearly defined and openly accessible are critical first steps. Equally important is employing a valid assessment methodology to evaluate the final model.
</p>

??? Note "Further Reading"
	In biological research, there are two main types of evaluation scenarios for ML models: 
	
	1. __Experimental Validation:__ This involves validating the predictions made by the ML model through laboratory experiments. Although highly desirable, this approach is often beyond the scope of many ML studies.
	
	2. __Computational Assessment:__ This involves evaluating the model's performance using established metrics. This section focuses on computational assessment and highlights a few potential risks.
	
	When it comes to performance metrics, which are quantifiable indicators of a model's ability to address a specific task, there are numerous metrics available for various ML classification and regression problems. The wide range of options, along with the domain-specific knowledge needed to choose the right metrics, can result in the selection of inappropriate performance measures. It is advisable to use metrics recommended by critical assessment communities relevant to biological ML models, such as the Critical Assessment of Protein Function Annotation (CAFA) and the Critical Assessment of Genome Interpretation (CAGI).
	
	Once appropriate performance metrics are selected, methods published in the same biological domain should be compared using suitable statistical tests (e.g., Student’s t-test) and confidence intervals. Additionally, to avoid releasing ML methods that seem advanced but do not outperform simpler algorithms, it is important to compare these methods against baseline models and demonstrate their statistical superiority (e.g., comparing shallow versus deep neural networks).[@DOME]




## 4.1 Evaluation method

<p style='text-align: justify;'>
Evaluation of a ML model is the process of assessing its performance and effectiveness in making predictions or classifications based on new, unseen data. 
Proper evaluation is crucial to ensure that the model generalizes well and performs as expected in real-world applications.
</p>

<ins>Key Questions</ins>

- How was the method __evaluated__ (for example cross-validation, independent dataset, novel experiments)?

!!! example "From Example Publication"
	Independent dataset

## 4.2 Performance measures

<p style='text-align: justify;'>
The choice of evaluation metrics depends on the type of problem (regression or classification) and the specific goals of the analysis.
</p>

| Regression Metrics   | Classification Metrics	|
|-------|---------|
| Mean Absolute Error (MAE)  | Accuracy|
| Mean Squared Error (MSE)|  Precision |
| Root Mean Squared Error (RMSE)| Recall (Sensitivity)  |
| R-squared (R<sup>2</sup>) |  F1 Score |


<ins>Key Questions</ins>

- Which __performance metrics__ are reported (Accuracy, sensitivity, specificity, etc.)? 
- Is this set __representative__ (for example, compared to the literature)?

!!! example "From Example Publication"
	Balanced Accuracy, Precision, Sensitivity, Specificity, F1, MCC.

## 4.3 Comparison

<p style='text-align: justify;'>
Comparison typically refers to the evaluation of different models, algorithms, or configurations to identify which one performs best for a specific task. 
This process is essential for selecting the most suitable approach for a given problem, optimizing performance, and understanding the strengths and weaknesses of various methods. 
</p>

<ins>Key Questions</ins>

- Was a comparison to __publicly available__ methods performed on benchmark datasets? 
- Was a comparison to __simpler baselines__ performed?

!!! example "From Example Publication"
	DisEmbl-465, DisEmbl-HL, ESpritz Disprot, ESpritz NMR, ESpritz Xray, Globplot, IUPred long, IUPred short, VSL2b. Chosen methods are the methods from which the meta prediction is obtained.

## 4.4 Confidence

<p style='text-align: justify;'>
Confidence in the context of ML refers to the measure of certainty or belief that a model's prediction is accurate. 
It quantifies the model's certainty regarding its output, which is particularly important in classification tasks, where decisions need to be made based on predicted class probabilities.
This can be supported with medthods such as confidence intervals and statistical significance.
</p>

<ins>Key Questions</ins>

- Do the performance metrics have __confidence intervals__? 
- Are the results __statistically significant__ to claim that the method is superior to others and baselines?

!!! example "From Example Publication"
	Not calculated.

## 4.5 Availability of evaluation

<p style='text-align: justify;'>
Availability of evaluation in ML refers to the accessibility and readiness of tools, frameworks, datasets, and methodologies used to assess the performance of ML models. 
This encompasses various aspects, from the datasets used for evaluation to the metrics and software tools that facilitate the evaluation process. 
</p>

<ins>Key Questions</ins>

- Are the __raw evaluation files__ (for example, assignments for comparison and baselines, statistical code, confusion matrices) available? 
- If yes, __where__ (for example, URL) and __how__ (license)?

!!! example "From Example Publication"
	Not.


<br> 