# In The Name Of Deep Learning
This project is done as a part of the final project of the course computer vision (B-KUL-H02A5A) of MOAI at KU Leuven.
In this project, a multi-label classifier and a segmentor is trained on PASCAL VOC 2009 dataset avaialable at [PASCAL VOC 2009](http://host.robots.ox.ac.uk/pascal/VOC/voc2009/VOCtrainval_11-May-2009.tar)

Both segmentation and classification models are developed and tested on Google Colab. 

## 1) Multi - Label Classification
In classification, the model is first trained from the scratch with the dataset. Later the same model is trained using transfer learning.
The models are trained using VGG16 architectue. For transfer learning, the model layers are frozen with "imagenet" weights. Both the model results are compared in the end. The results of the model are given [here](Image_Classification/README.md). The model training and evaluation procedure is given in [Multi_Label_Classification_Pascal_VOC](Image_Classification/Multi_Label_Classification_Pascal_VOC.ipynb).

## 2) Semantic Segmentation 
Similar to classification, the models are first trained from the scratch with the dataset and then using transfer learning.
The models are trained using VGG-UNet architectue. For transfer learning, only the encoder layers of the model are frozen with "imagenet" weights. 
Both the model results are compared in the end. The results of the model are given [here](Image_Segmentation/README.md). The model training and evaluation procedure is given in [Semantic Segmentation_Pascal_VOC](Image_Segmentation/Segmentation_Pascal_VOC.ipynb).


## 3)Adversarial Attack

After training the classifier, a encoder-decoder model is trained to generate noise for specific classes of images. These noisy images are then added to the original images to fool the classifier. The adversarial attack is perfomed on the classifier using the images of **"Bird"** and **"Aeroplane"**. The evaluation results for the same is given [here](Image_Classification/README.md)

