### 20211019

## N. Liu, J. Han, D. Zhang, S. Wen and T. Liu, "[Predicting eye fixations using convolutional neural networks](https://ieeexplore.ieee.org/document/7298633)," (2015)

### What did they do and how did they confirm?<br>
 - Ensembles of CNNs using different resolution but same images could learn about bottom-up saliency and top-down features simultaneously and improve the saliency accuracy. Feature visualization each layer confirmed that targetted features were contained. Also, the effect from the number of resolutions and the number of convolution layers were investigated.
 
   - [Background]
     - As the backgwround, the previous researches used hand-crafted features, which could be difficult to apply to the different complex images.
     - High-level info extraction was still hard for the representation limitation of shallower network (because GPU was developing, not having today's performance).

### What is new? (or what is previous issue)<br>

 - Multi-resolution CNNs (ensemble of different resolution images) enabled to integrate low-level, bottom-up saliency and top-down factors at the same time.

### Interesting techniques, ideas and methods<br>
 - Same image regions of fixed size but different resolutions were extracteda and used as the input data.

### Interesting hypothesis and analysis<br>
 - Ensemble of same images with different resolution looks like data-augmentation, though this model training also utilized horizental flipping.

### Waht is the limitation I think?<br>
 - The network used in the experiment was shallow (3 conv layers and 2 FC layers), and it looks like not having enough representation ability. The reason using such network seems to come from computational resource issue in those days.

### What would I want to know furthermore?<br>
 - Latest saliency model using DNNs

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


