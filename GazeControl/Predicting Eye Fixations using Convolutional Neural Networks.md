### 20211019

## N. Liu, J. Han, D. Zhang, S. Wen and T. Liu, "[Predicting eye fixations using convolutional neural networks](https://ieeexplore.ieee.org/document/7298633)"

### Summary<br>


### What is new? (or what is previous issue)<br>
 
   The author's keypoints are as follows,
 
   - Large depths which enables to learn complex features from scenes
     - Previous study utilized shallower network, and the semantic feature extracting was difficult<br>
   - Different size kernels in parallel by using the inception layer<br>
     - Previous one ensembled CNN output
   - Large receptive field by two dilated conv to capture the global context of scenes for a saliency map<br>

### Interesting techniques, ideas and methods<br>
     

### Interesting hypothesis and analysis<br>

### What would I want to know furthermore?<br>

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


