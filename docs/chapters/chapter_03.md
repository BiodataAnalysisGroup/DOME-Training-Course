<p style='text-align: justify;'>
Good overall performance of the trained model and its ability to generalize well to unseen data are important factors that undoubtedly affect the applicability of any proposed ML research. However, a few other important aspects related to ML models must be kept in mind. 
</p>

??? Note "Further Reading"
	Equally important aspects related to ML models are their interpretability and reproducibility. 
	Interpretable models can infer causal relationships from the data and can output logical reasoning for each of their predictions. 
	They are especially relevant in areas of discovery such as drug design and diagnostics. Conversely, black box models often give accurate predictions but may not provide insight in a way humans can understand into why they made the predictions. Both interpretable and black box models are discussed in more detail elsewhere. 
	However, developing recommendations on the choice of black box or interpretability is not straightforward as both have their merits. 
	The main recommendation would be that there is a statement as to whether the model type is black box or interpretable, and if it is interpretable, clear examples of interpretable output should be given.

	Reproducibility is a key component for ensuring research outcomes can be further used and validated by the wider community. Poor model reproducibility extends beyond the documentation and reporting of the involved parameters, hyperparameters and optimization protocol. 
	Lacking access to the various components of a model (source code, model files, parameter configurations and executables), as well as having steep computational requirements for executing the trained models to generate predictions based on new data, can make reproducibility of the model either limited or practically impossible.[@DOME]


## 3.1 Interpretability

- Is the model __black box__ or __interpretable__? 
- If the model is interpretable, can you give clear __examples__ of this?

## 3.2 Output

- Is the model __classification__ or __regression__?

## 3.3 Execution time

-  How much __time__ does a single representative prediction require on a standard machine (for example, seconds on a desktop PC or high-performance computing cluster)?


## 3.4 Availability of software

- Is the __source code__ released? 
- Is a __method to run__ the algorithm (executable, web server, virtual machine or container instance) released? 
- If yes, __where__ (for example, URL) and __how__ (license)?


## 3.5 Example

Here's an example of how the DOME corresponding section would be filled for this publication [@MobiDB] :

|      |        |      |
|-------    |-------    |---------  |
| Model  | Interpretability | Transparent, in so far as meta-prediction is concerned. Consensus and post processing over other methods predictions (which are mostly black boxes). No attempt was made to make the meta-prediction a black box.   |
|     	 | Output | Classification, i.e. residues thought to be disordered. |
|     	 | Execution time | ca. 1 second per representative on a desktop PC.|
|     	 | Availability of software |Yes, URL: http://protein.bio.unipd.it/mobidblite/. <br>  Bespoke license free for academic use|


<br> 