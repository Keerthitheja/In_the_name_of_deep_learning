# Multi - Label Classification on PASCAL VOC (2009)

The .ipynb notebook can be run directly on Google Colab. The dataset is donloaded automatically and saved to the local colab session. 

The classifier is trained using VGG16 architecture as backbone for both from the scratch and transfer leaerning methods.

## Training the model from scratch
The model results are given below. The model gives an training accuracy of 81% which is rather high compared to other evaluation metrices like f1 score and precision. The dataset is imbalanced due to large number of data samples for class **Person** compared to other classes.

The training curves are as below

![alt-text-1](../output_Images/class_sc.png "Training curve 1") ![alt-text-2](../output_Images/class_sc1.png "Training curve 2")

**Test set loss          : 17.46% <br />
Test set accuracy      : 94.82% <br />
Test set f1_m          : 73.11% <br />
Test set precision_m   : 67.95% <br />**

Some of the model predictions on test set is

![alt-text](../output_Images/class_sc_out.png "Model Output")

## Training the model using Transfer Learning
The model results are given below. The performance of the model get better with Transfer Learning.

The training curves are as below

![alt-text-1](../output_Images/class_tl.png "Training curve 1") ![alt-text-2](../output_Images/class_tl1.png "Training curve 2")

**Test set loss        : 8.67% <br />
Test set accuracy      : 97.62% <br />
Test set F1 score      : 85.37% <br />
Test set precision     : 92.13% <br />**

Some of the model predictions on test set is

![alt-text](../output_Images/class_tl_out.png "Model Output")

# Adversarial Attack

A encoder-decoder model is trained to generate a noisy image for train and test sets. This is done selectively on two classes of images (**aeroplane and bird**). The classifier is fooled with this noisy images
for its performance. Two sets of adversariaries are trained for train and test sets. 

The adversarial images are as shown below

![alt-text-1](../output_Images/adv_1.png "Aeroplane") ![alt-text-2](../output_Images/adv_2.png "Bird")



The adversarial attack results on the classifier are as given below

## Train set Adversary

| Results on Actual images | Results on Noised images |
| ------------------------ | ------------------------ |
| Accuracy   : **97.42%** | Accuracy   : **97.11%** |
| F1 score   : **81.23%** | F1 score   : **79.02%** |
| Precision  : **72.32%** | Precision  : **70.11%** |

## Test set Adversary

| Results on Actual images | Results on Noised images |
| ------------------------ | ------------------------ |
| Accuracy    : **92.47%** | Accuracy    : **92.47%** |
| F1 score    : **52.17%** | F1 score    : **50.51%** |
| Precision   : **44.40%** | Precision   : **43.60%** |



