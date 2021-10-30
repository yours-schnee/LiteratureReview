### 20211029

## D. Bau, B. Zhou, A. Khosla, A. Oliva, and A. Torralba, "[Network Dissection: Quantifying Interpretability of Deep Visual Representations](https://arxiv.org/abs/1704.05796v1)," (2017)

### What did they do and how did they confirm?<br>
 - Proposed frameworks to interprete deep representation and evaluate the interpretability through disentagled representations, which is a visualization method between each hidden unit and a set of semantic concepts by using a broadly and densely labeled dataset.
 - Scored by Unit Interpretability (IoU, unique detector) as follows,

![Example](https://github.com/yours-schnee/LiteratureReview/blob/imgs/imgs/IoU.png?raw=true)

   where L<sub>c</sub>(x) is input-resolution annotation mask and M<sub>k</sub>(x) is a thresholded binary segmentation.


### What is new? (or what is previous issue)<br>


### Interesting techniques, ideas and methods<br>
     

### Interesting hypothesis and analysis<br>

### What would I want to know furthermore?<br>

### Experimental settings
#### Dataset<br>
  - The Broadly and Densely Labeled Dataset (Broden)
  - This is motivated from the purpose to confirm the alignment with low-level concepts (color) and higher-level ones (object)
    - Unification of the followings:
      - ADE
      - Ipen-Surfaces
      - Pascal-COntext
      - Pascal-Part
      - Describable Textures Dataset
 
#### Initialization<br>
  - TRandom initialization by [Convergent Learning: Do different neural networks learn the same representations?](https://arxiv.org/abs/1511.07543v3#)

#### Ebaluation method<br>
 

### My Citation<br>
