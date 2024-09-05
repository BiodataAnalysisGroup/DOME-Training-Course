<p style='text-align: justify;'>
In the implementation of a robust and trustworthy ML method, a comprehensive data description, a correct optimization protocol, and a clearly defined (and open-access) model are critical first steps; however, equally important is a valid assessment methodology for any final model.
</p>

??? Note "Further Reading"
	There are two types of evaluation scenarios in biological research. 
	The __first__ is the experimental validation of the predictions made by the ML model in the laboratory. 
	This is highly desirable but beyond the scope of many ML studies. 
	The __second__ is a computational assessment of the model performance using established metrics. The following deals with the latter. There are a few possible risks in computational evaluation.
	
	To start with performance metrics—that is, the quantifiable indicators of a model’s ability to solve the given task—there are dozens of metrics available for assessing different ML classification and regression problems. 
	The plethora of options available, combined with the domain-specific expertise that might be required to select the appropriate metrics, can lead to the selection of inadequate performance measures. 
	Often, there are critical assessment communities advocating certain performance metrics for biological ML models—for example, Critical Assessment of Protein Function Annotation (CAFA) and Critical Assessment of Genome Interpretation (CAGI)—and we recommend that a new algorithm should use metrics from the literature and community-promulgated critical assessments.[@DOME]




## 4.1 Evaluation method

- How was the method __evaluated__ (for example cross-validation, independent dataset, novel experiments)?

## 4.2 Performance measures

- Which __performance metrics__ are reported? 
- Is this set __representative__ (for example, compared to the literature)?

## 4.3 Comparison

- Was a comparison to __publicly available__ methods performed on benchmark datasets? 
- Was a comparison to __simpler baselines__ performed?

## 4.4 Confidence

- Do the performance metrics have __confidence intervals__? 
- Are the results __statistically significant__ to claim that the method is superior to others and baselines?


## 4.5 Availability of evaluation

- Are the __raw evaluation files__ (for example, assignments for comparison and baselines, statistical code, confusion matrices) available? 
- If yes, __where__ (for example, URL) and __how__ (license)?


