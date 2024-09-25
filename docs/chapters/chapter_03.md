<p style='text-align: justify;'>
Good overall performance and the model's ability to generalize well to unseen data are crucial factors that significantly impact the applicability of any proposed ML research. However, several other important aspects related to ML models must also be considered.
</p>

??? Note "Further Reading"
	Equally important aspects of ML models include their interpretability and reproducibility. Interpretable models can identify causal relationships in the data and provide logical explanations for their predictions, which is especially valuable in fields like drug design and diagnostics. In contrast, black box models, while often accurate, may not offer understandable insights into the reasons behind their predictions. Both types of models are discussed in more detail elsewhere, and choosing between them involves weighing their respective benefits. The key recommendation is to clearly state whether the model is a black box or interpretable, and if it is interpretable, to provide clear examples of its outputs.
	
	Reproducibility is crucial for ensuring that research outcomes can be effectively utilized and validated by the broader community. Challenges with model reproducibility go beyond merely documenting parameters, hyperparameters, and optimization protocols. Limited access to essential model components (such as source code, model files, parameter configurations, and executables) and high computational demands for running trained models on new data can severely restrict or even prevent reproducibility.[@DOME]


## 3.1 Interpretability

- Is the model __black box__ or __interpretable__? 
- If the model is interpretable, can you give clear __examples__ of this?

|  Interpretability Section Example  |
|---------  |
| Transparent, in so far as meta-prediction is concerned. Consensus and post processing over other methods predictions (which are mostly black boxes). No attempt was made to make the meta-prediction a black box.   |


## 3.2 Output

- Is the model __classification__ or __regression__?

|  Output Section Example  |
|---------  |
| Classification, i.e. residues thought to be disordered. |

## 3.3 Execution time

-  How much __time__ does a single representative prediction require on a standard machine (for example, seconds on a desktop PC or high-performance computing cluster)?

|  Execution time Section Example  |
|---------  |
| ca. 1 second per representative on a desktop PC.|

## 3.4 Availability of software

- Is the __source code__ released? 
- Is a __method to run__ the algorithm (executable, web server, virtual machine or container instance) released? 
- If yes, __where__ (for example, URL) and __how__ (license)?

|  Availability of software Section Example  |
|---------  |
|Yes, URL: http://protein.bio.unipd.it/mobidblite/. <br>  Bespoke license free for academic use|


<br> 