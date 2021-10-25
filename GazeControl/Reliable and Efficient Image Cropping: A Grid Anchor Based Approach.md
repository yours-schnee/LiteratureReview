###20211025

## H. Zeng, L. Li, Z. Cao, and L. Zhang , "[Reliable and Efficient Image Cropping: A Grid Anchor Based Approach](https://ieeexplore.ieee.org/document/8953733/authors#authors)," (2019)

### What is new? (or what is previous issue)<br>


### Interesting techniques, ideas and methods<br>

### Interesting hypothesis and analysis<br>

### Waht is the limitation I think?<br>

### What would I want to know furthermore?<br>

### Experimental settings
#### Dataset<br>
  - Collected Flickr images, which were automatically cropped by annotation tool and evaluated as the mean opinitionscore (MOS) by 19 human annotators.
 
#### Initialization<br>
  - Encoder part: VGG16 pretrained on ImageNet
  - Decoder: Gaussian with mean 0 and std 0.01

#### Ebaluation method<br>
 - average Spearman’s rank-order correlation coefficient (SRCC). The
 - return K of top-N accuracy (ACC<sub>CC</sub><sub>K/N</sub>)
 - 
![ACC<sub>CC</sub><sub>K/N</sub>](https://github.com/yours-schnee/LiteratureReview/blob/imgs/imgs/DeepVisualAttentionPrediction.png?raw=true)

### My Citation<br>
 [1] [Salient Object Detection: A Benchmark](https://ieeexplore.ieee.org/abstract/document/7293665?casa_token=Amwukp6MlIQAAAAA:L5erpcJswXlxjkm2OAnsoN_b-ELrJN9LU72LtTcAxDXoPvhDeRqf7cZgcCQCSFlMOWApzwYyXvk)<br>
 [2] [Holistically-nested edge detection](https://openaccess.thecvf.com/content_iccv_2015/html/Xie_Holistically-Nested_Edge_Detection_ICCV_2015_paper.html)<br>
 [3] [Deeply-Supervised Nets](http://proceedings.mlr.press/v38/lee15a.html)
