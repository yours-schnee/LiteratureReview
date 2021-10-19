### 20211019

## S. S. S. Kruthiventi, K. Ayush and R. V. Babu, "DeepFix: A Fully Convolutional Neural Network for Predicting Human Eye Fixations," IEEE Transactions on Image Processing, vol. 26, (9), pp. 4446-4456, 2017

- Summary
 The bottom-up saliency approach using CNNs could automatically learn about target features, instead of the classical hand-crafted ones.
 To approach this, location-biased convolution
 
 The ablation study showed that the LBC overcame the traditional techniques of bias addition.


- What is new? (what is previous issue)
 This study applied the similar structure to VGG-19 (very deep structure), comparing with the previous study.
 The inception layers can provid the multi-scale semantic features, instead of the CNN ensemble (previous study)
 Also, to prevent from responding to the specific pattern of location, the fully-connected layer (location-biased convolution) were combined in front of the last 1x1 convolutionl layer.

 (1) Large depths which enables to learn complex features from scenes (previous study utilized shallower network, so the semantic feature extracting seemed be difficult)
 (2) Different size kernels in parallel by using the inception layer
 (3) Large receptive field to capture the global context of scenes for a saliency map

- Interesting techniques, ideas and methods

 (1) The dilated convolution in the 5-th layer, which seems to aim to reduce the weight initialization tasks.
 However, Fisher and Vladlen [1] used this hole as the support for seeing a wide range of information while maintaining a high-frequency.
 Which effect is more influential to this study result?

 (2) The LBC layers, which are dilated conv layers (6 hole), were introduced based on the neuroscience literature.
     

- What is limitation I felt?

- Interesting hypothesis and analysis
 Saliency is well-captured when the semantics are considered from multiple-scales.
 This may follow one hypothesis of visual working memory, which combines object details from different viewpoint to understand objects [2].

- What would I want to know furthermore?
 

- Dataset
 SALICON, CAT2000, MIT1003, MIT300
 
- Ebaluation method
 The followings were applied: Earth Mover’s Distance, Normalized Scanpath Saliency, Linear Correlation Coefficient, Similarity metric, and AUC.
 Also, ablation analysis for the effect of LBD layers was done.
 

- Citation
  [Multi-Scale Context Aggregation by Dilated Convolutions](https://arxiv.org/abs/1511.07122v3)
  [Visual working memory as visual attention sustained internally over time](https://pubmed.ncbi.nlm.nih.gov/21295047/)
