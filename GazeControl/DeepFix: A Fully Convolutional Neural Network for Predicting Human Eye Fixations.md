### 20211019

## S. S. S. Kruthiventi, K. Ayush and R. V. Babu, "[DeepFix: A Fully Convolutional Neural Network for Predicting Human Eye Fixations](https://ieeexplore.ieee.org/document/7937829)"

### Summary<br>
 Whether the wide-range information by the location-biased convolution (LBC) layers could improve a saliency map was investigated.
 The ablation study showed that the LBC layers contributed to its performance rather than the traditional techniques of bias addition.

### What is new? (or what is previous issue)<br>
 This study applied the very deep structure, which has the inception blocks that can provid the multi-scale semantic features.
 The two fully-convolution layers with a dilated conv (LBS) layer were combined after inception block.
 This aims to prevent from responding to the specific pattern of location. <br>
 
   The author's keypoints are as follows,
 
   - Large depths which enables to learn complex features from scenes
     - Previous study utilized shallower network, and the semantic feature extracting was difficult<br>
   - Different size kernels in parallel by using the inception layer<br>
     - Previous one ensembled CNN output
   - Large receptive field by two dilated conv to capture the global context of scenes for a saliency map<br>

### Interesting techniques, ideas and methods<br>
 (1) The dilated convolution in the 5-th layer, which seems to aim to reduce the weight initialization tasks.
 However, Fisher and Vladlen [[1]](https://arxiv.org/abs/1511.07122v3) used this hole as the support for seeing a wide range of information while maintaining a high-frequency.
 Which effect is more influential to this study result?<br>
 (2) The LBC layers, which are dilated conv layers (6 hole), were introduced based on the neuroscience literature.
     

### Interesting hypothesis and analysis<br>
 Saliency is well-captured when the semantics are considered from multiple-scales.
 This may follow one hypothesis of visual working memory, which combines object parts (details?) from different viewpoint to understand objects [[2]](https://pubmed.ncbi.nlm.nih.gov/21295047/).

### What would I want to know furthermore?<br>
  - Whether saliency and classification match where they are looking
    - [Question] Does the narrowing of the focus by a saliency make classifier hard to identify targets?

### Experimental settings
#### Dataset<br>
  - 1st stage: SALICON (pretraining)
  - 2nd stage: CAT2000, MIT1003, MIT300 (train & test)
 
#### Initialization<br>
  - The first 16 Convolution layers: VGG16's weights
  - Inception block: zero mean Gaussian distribution
  - LBC layers: zero mean Gaussian distribution

#### Ebaluation method<br>
 - The followings were applied: Earth Mover’s Distance, Normalized Scanpath Saliency, Linear Correlation Coefficient, Similarity metric, and AUC.
 - Ablation analysis for the effect of LBD layers was done.
 

### My Citation<br>
  [1] [Multi-Scale Context Aggregation by Dilated Convolutions](https://arxiv.org/abs/1511.07122v3)<br>
  [2] [Visual working memory as visual attention sustained internally over time](https://pubmed.ncbi.nlm.nih.gov/21295047/)<br>
