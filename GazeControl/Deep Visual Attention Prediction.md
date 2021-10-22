### 20211020

## W. Wang and J. Shen, "[Deep Visual Attention Prediction](https://ieeexplore.ieee.org/document/8240654)," (2017)


### What did they do and how did they confirm?<br>
 - Extracting features with multi-scale and multi-level from diffirent layers are decoded as saliency maps and they are combined by a fusion layer. Each decoded intermediate saliency and final saliency are minimized by the cross-entropy.
 - Performance comparison with other models
 - Evaluate each component contribution of the proposed model

### What is new? (or what is previous issue)<br>
 - Multi-level saliency prediction by a signle netwok with an encoder-decoder structure.
  - Decoder is learnable because of preferablity to the previous fixed interpolation kernel
  - Decrease computational load due to dimension reduction (decoder's general nature)

### Interesting techniques, ideas and methods<br>
 - Fusion of three intermediate layer outputs are simply multiplied by trainable weights and finally merged.

### Interesting hypothesis and analysis<br>
 - Due to the large depth and multi-level features, generated saliency maps were very localized rather than other comparator models.
 - In ablation study, average prediction of multi-layer outouts overcame a single-layer outputs, and the combination between multi-scale prediction could improve s-AUC of saliency map more.

### Waht is the limitation I think?<br>
 - As the authors said, generated saliency maps limited to very local positions, and it looks like having the difficulty for object detection.
  (But this study set the purpose as predicting human eye traking [1])

### What would I want to know furthermore?<br>
 - Other adopted netwrok like [2] and [3]

### Experimental settings
#### Dataset<br>
  - SALICON (for trained)
  - MIT300, MIT1003
  - TORONTO: [Saliency Based on Information Maximization](https://proceedings.neurips.cc/paper/2005/file/0738069b244a1c43c83112b735140a16-Paper.pdf)
  - PASCAL-S
  - DUT-OMRON
 
#### Initialization<br>
  - Encoder part: VGG16 pretrained on ImageNet
  - Decoder: Gaussian with mean 0 and std 0.01

#### Ebaluation method<br>
 - Earth Movers Distance
 - Normalized Scanpath Saliency
 - Similarity Metric
 - Linear Correlation Coefficient
 - AUC-Judd
 - AUC-Borji
 - shuffled-AUC

### My Citation<br>
 [1] [Salient Object Detection: A Benchmark](https://ieeexplore.ieee.org/abstract/document/7293665?casa_token=Amwukp6MlIQAAAAA:L5erpcJswXlxjkm2OAnsoN_b-ELrJN9LU72LtTcAxDXoPvhDeRqf7cZgcCQCSFlMOWApzwYyXvk)<br>
 [2] [Holistically-nested edge detection](https://openaccess.thecvf.com/content_iccv_2015/html/Xie_Holistically-Nested_Edge_Detection_ICCV_2015_paper.html)<br>
 [3] [Deeply-Supervised Nets](http://proceedings.mlr.press/v38/lee15a.html)
