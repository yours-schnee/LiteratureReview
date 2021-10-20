### 20211019

## N. Liu, J. Han, D. Zhang, S. Wen and T. Liu, "[Predicting eye fixations using convolutional neural networks (2015)](https://ieeexplore.ieee.org/document/7298633)"

### Summary<br>
 - Ensembles of CNNs using different resolution but same images could learn about bottom-up saliency and top-down features and  improve the saliency accuracy. Feature visualization each layer confirmed that targetted features were contained. Also,
 
   - [Background]
     - As the backgwround, the previous researches used hand-crafted features, which could be difficult to apply to the different complex images.
     - In those days, high-level info extraction was still hard for the representation limitation of shallower network (because GPU was developing, not having today's performance).

### What is new? (or what is previous issue)<br>
 
   The author's keypoints are as follows,
 
   - Large depths which enables to learn complex features from scenes
     - Previous study utilized shallower network, and the semantic feature extracting was difficult<br>
   - Different size kernels in parallel by using the inception layer<br>
     - Previous one ensembled CNN output
   - Large receptive field by two dilated conv to capture the global context of scenes for a saliency map<br>

### Interesting techniques, ideas and methods<br>
     

### Interesting hypothesis and analysis<br>

### Waht is the limitation I think?<br>
 - The network used in the experiment was shallow (3 conv layers and 2 FC layers), and it looks like not having enough representation ability. The reason using such network seems to come from computational resource issue in those days.

### What would I want to know furthermore?<br>

### Experimental settings
#### Dataset<br>
  - MIT dataset: [Learning to predict where humans look](https://dspace.mit.edu/handle/1721.1/62546)
  - [Saliency Based on Information Maximization](https://proceedings.neurips.cc/paper/2005/file/0738069b244a1c43c83112b735140a16-Paper.pdf)
  - [Predicting human gaze using low-level saliency combined with face detection](https://proceedings.neurips.cc/paper/2007/hash/708f3cf8100d5e71834b1db77dfa15d6-Abstract.html)
  - [An Eye Fixation Database for Saliency Detection in Images](https://link.springer.com/chapter/10.1007/978-3-642-15561-1_3)
 
#### Initialization<br>
  - Pretrained on MIT dataset, and fine-tuning was conducted to other dataset. This reason came from the richness of images among the four datasets. 

#### Ebaluation method<br>
 - Shuffled A-AUC and average shuffled-AUC
 - Feature visualization
 

### My Citation<br>


