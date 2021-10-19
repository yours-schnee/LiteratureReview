### 20211019

## S. S. S. Kruthiventi, K. Ayush and R. V. Babu, "[DeepFix: A Fully Convolutional Neural Network for Predicting Human Eye Fixations](https://ieeexplore.ieee.org/document/7937829)"

- Summary<br>
 The bottom-up saliency approach using CNNs could automatically learn about target features, instead of the classical hand-crafted ones.
 To approach this, location-biased convolution
 The ablation study showed that the LBC overcame the traditional techniques of bias addition.

- What is new? (or what is previous issue)<br>
 This study applied the similar structure to VGG-19 (very deep structure), which has the inception layers that can provid the multi-scale semantic features, instead of the CNN ensemble (previous study).
 Also, to prevent from responding to the specific pattern of location, the two fully-convolution layers with a dilated conv (location-biased convolution) were combined in front of the last 1x1 convolutionl layer.<br>
 
  - Large depths which enables to learn complex features from scenes
    - previous study utilized shallower network, and the semantic feature extracting was difficult<br>
  - Different size kernels in parallel by using the inception layer<br>
  - Large receptive field by two dilated conv to capture the global context of scenes for a saliency map<br>

- Interesting techniques, ideas and methods<br>
 (1) The dilated convolution in the 5-th layer, which seems to aim to reduce the weight initialization tasks.
 However, Fisher and Vladlen [1] used this hole as the support for seeing a wide range of information while maintaining a high-frequency.
 Which effect is more influential to this study result?<br>
 (2) The LBC layers, which are dilated conv layers (6 hole), were introduced based on the neuroscience literature.
     

- What is limitation I felt?<br>

- Interesting hypothesis and analysis<br>
 Saliency is well-captured when the semantics are considered from multiple-scales.
 This may follow one hypothesis of visual working memory, which combines object details from different viewpoint to understand objects [2].

- What would I want to know furthermore?<br>
  - Whether saliency and classification match where they are looking
    - Does the narrowing of the focus by a saliency make classifier hard to identify targets?

- Dataset<br>
  - 1st stage: SALICON (pretraining)
  - 2nd stage: CAT2000, MIT1003, MIT300 (train & test)
 
- Initialization<br>
  - The first 16 Convolution layers: VGG16's weights
  - Inception block: zero mean Gaussian distribution
  - LBC layers: zero mean Gaussian distribution

- Ebaluation method<br>
 The followings were applied: Earth Mover’s Distance, Normalized Scanpath Saliency, Linear Correlation Coefficient, Similarity metric, and AUC.
 Also, ablation analysis for the effect of LBD layers was done.
 

- Citation<br>
  [1] [Multi-Scale Context Aggregation by Dilated Convolutions](https://arxiv.org/abs/1511.07122v3)<br>
  [2] [Visual working memory as visual attention sustained internally over time](https://pubmed.ncbi.nlm.nih.gov/21295047/)<br>
