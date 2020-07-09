# Multi - Label Classification on PASCAL VOC (2009)

The .ipynb notebook can be run directly on Google Colab. The dataset is donloaded automatically and saved to the local colab session. 

The classifier is trained using VGG16 architecture as backbone for both from the scratch and transfer leaerning methods.

## Training the model from scratch
The model results are given below. The model gives an training accuracy of 81% which is rather high compared to other evaluation metrices like f1 score and precision. The dataset is imbalanced due to large number of data samples for class **Person** compared to other classes.

The training curves are as below

![alt-text-1](../output_Images/class_sc.png "Training curve 1") ![alt-text-2](../output_Images/class_sc1.png "Training curve 2")

Test set loss          : 17.46%
Test set accuracy      : 94.82%
Test set f1_m          : 73.11%
Test set precision_m   : 67.95%`

Some of the model predictions on test set is

![alt-text](../output_Images/class_sc_out.png "Model Output")

## Training the model using Transfer Learning
The model results are given below. The performance of the model get better with Transfer Learning.

The training curves are as below

![alt-text-1](../output_Images/class_tl.png "Training curve 1") ![alt-text-2](../output_Images/class_tl1.png "Training curve 2")

Test set loss          : 8.67%
Test set accuracy      : 97.62%
Test set f1_m          : 85.37%
Test set precision_m   : 92.13%

Some of the model predictions on test set is

![alt-text](../output_Images/class_tl_out.png "Model Output")

# Adversarial Attack


