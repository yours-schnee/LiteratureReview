###20211025

## H. Zeng, L. Li, Z. Cao, and L. Zhang , "[Reliable and Efficient Image Cropping: A Grid Anchor Based Approach](https://ieeexplore.ieee.org/document/8953733/authors#authors)," (2019)

### What is new? (or what is previous issue)<br>
  - Automatic ideal image cropping method based on the rule of thirds by using CNNs
  - The performance was firstly investigated by ablation study that changed feature map output layers  and RoD parameters used in image cropping and RoI.
  - The proposal's performance was alos evaluated by the cmparison with other Grid Anchor based Image Cropping (GAIC) models.
    -[Background] Conventional methods did not focus on a network for image cropping itself.

![Arch](https://github.com/yours-schnee/LiteratureReview/blob/imgs/imgs/Reliable_and_Efficient_Image_Cropping.png?raw=true)


### Interesting techniques, ideas and methods<br>
  - Discarded information (RoD) was also utilized to train the proposed model. This motivation comes from the reason that cropping also needs to consider the discarded info. The most right of the following shows the bad cropping example.

![Example](https://github.com/yours-schnee/LiteratureReview/blob/imgs/imgs/Reliable_and_Efficient_Image_Cropping_example.png?raw=true)

### Interesting hypothesis and analysis<br>
  - VGG16 was better than ResNet50, which is considered by overfitting to their dataset.

### Waht is the limitation I think?<br>
  - It is unclear whether cropped images could capture targets well or not in the context of object detection, but this is motivated on redundancy, content preservation, and aspect ratio. It may be a little different from the condition of a saliency map because this image cropping7s assumption is that targets would also be contained in images.

### What would I want to know furthermore?<br>
  - Return to saliency map generation approach

### Experimental settings
#### Dataset<br>
  - Original data collected from Flickr images, which were automatically cropped by annotation tool and evaluated as the mean opinitionscore (MOS) by 19 human annotators.
 
#### Initialization<br>
  - Encoder part: VGG16 pretrained on ImageNet
  - Decoder: Gaussian with mean 0 and std 0.01

#### Ebaluation method<br>
 - average Spearman’s rank-order correlation coefficient (SRCC). The
 - return K of top-N accuracy (ACC<sub>CC</sub><sub>K/N</sub>)
 - 
![ACC<sub>CC</sub><sub>K/N</sub>](https://github.com/yours-schnee/LiteratureReview/blob/imgs/imgs/ACCKN.png?raw=true)

### My Citation<br>
