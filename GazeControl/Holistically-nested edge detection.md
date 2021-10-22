### 20211020

## S. Xie and Z. Tu, "[Holistically-nested edge detection](https://ieeexplore.ieee.org/document/7410521)," (2015)


### What did they do and how did they confirm?<br>
  - Edge detection using CNNs, which have several side-output layers after conv layers to generate multi-scale edges. The multiscale-outputs are fusined by a fusion layer. The results are compared with other approaches.
    - [Background]: less meaningful multi-scale responses provided by patch-based edge detection of CNNs because back-projection through the intermediate layer downgrades. This comes from the demand of edge detection that needs accurate edge pixel localization

### What is new? (or what is previous issue)<br>
  - Like ensemble, VGG-16 intermediate layers are connected to side output layer to trim target edges by each layer (conv1_2, conv2_2, conv3_3, conv4_3, and conv5_3)<br>
  
![Architecture](https://github.com/yours-schnee/LiteratureReview/blob/imgs/imgs/Holistically-nested_edge_detection.png?raw=true)


### Interesting techniques, ideas and methods<br>
  - Intermediate output deatures are utilized to generate multi-scale edge figures and finally merged one edge figure.

### Interesting hypothesis and analysis<br>
  - Each network layer has a role as a singleton network responsible for producing an edge map at a certain scale.
  - Deep learned features have the ability oto learn object boundary, and weak edges are omitted (from dropping performances of high recall regime).

### Waht is the limitation I think?<br>
  - Downsampling within CNNs looks like interfering the precise edge.

### What would I want to know furthermore?<br>
  - One paper I read ever before (publishment is after 2017) seemed to explain about any ensemble effects...

### Experimental settings
#### Dataset<br>
  - BSD500
  - NYU Depth
 
#### Initialization<br>
  - VGG-16

#### Ebaluation method<br>
  - ﬁxed contour threshold (ODS), pe
  - per-image best threshold (OIS)
  - Average precision
  - Precision, recall, and F-score

### My Citation<br>
