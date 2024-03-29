# KAGGLE-HPA-Single-Cell-Classification-2021
Kaggle HPA Single cell classification

Code competition


- Semi-supervised learning

- Weakly supervised learning

- Multi-instance multi-label image classification

- Transfer learning

- Cell segmentation


## Competition webpage:

https://www.kaggle.com/c/hpa-single-cell-image-classification

## Our solution:

https://www.kaggle.com/koltaibeatrix/hpa-single-cell-classification-submission-2


## Our team:

**Koltai Beatrix** @koltaib

**Horváth Adrienn** @Horadry

-------------------------------------------------------------------------------------------------------------------------------------------------

## Background

Differences in the location of proteins can give rise to such cellular heterogeneity. Proteins play essential roles in virtually all cellular processes. Often, many different proteins come together at a specific location to perform a task, and the exact outcome of this task depends on which proteins are present. Different subcellular distributions of one protein can give rise to great functional heterogeneity between cells. Finding such differences, and figuring out how and why they occur, is important for understanding how cells function, how diseases develop, and ultimately how to develop better treatments for those diseases.



## Dataset

The data in the Human Protein Atlas database is freely accessible:

https://www.proteinatlas.org/

Train and test images: 4 images belong together. Red, blue and yellow filters (images 1-3) show the location of some cell organelles and the green filter (image 4) shows the location of the protein.   

Train data: image level labels. Labels refer to cell organelles where the protein occours. 



## Objective

Our aim was to make predictions on protein organelle localization labels for each cell in the images.



## Programming language, frameworks

- Python
- Keras
- Pytorch
- Tensorflow




## Method

**1. Cell segmentation**

On the base of HPA Cellsegmentetor

   ```python
   !pip install "../input/hpacellsegmentatormaster/HPA-Cell-Segmentation-master"
   ```
**2. Transfer learning**

After degenerating the problem to a **multi-instance single-label problem** (Zhou et al. 2011) we used **EfficientnetB0** as base model for predicting the occurrence of a given label on the images, as a binary classification. 

Our aim was to inspect the effectiveness of the EfficientnetB0 in this task. We trained a new model for each label.






## Conclusion and future plans

With our hyperparameter setting the best performance of our model was:

| Base Models    | Loss   | Accuracy |
| -------------- | ------ | -------- |
| EfficientNetB0 | x.0000 | xx.00 %  |



Our EfficientB0 based model system proved to be a working but less effective method for the HPA Single Cell Classification task. 

Our future plan is to inspecting the effectiveness of other models so that we can improve the accuracy. 




## Contact

Beatrix Koltai and Adrienn Horváth


11.05.2021
