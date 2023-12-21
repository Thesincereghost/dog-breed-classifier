# CNN to classify the breed of a dog

### Table of Contents

1. [Installation](#installation)
2. [Project Motivation](#motivation)
3. [File Descriptions](#files)
4. [Conclusion](#Conclusion)
5. [Licensing, Authors, and Acknowledgements](#licensing)

## Installation <a name="installation"></a>

+ Python version - 3.9.18
+ Libraries used - pandas, numpy, scikit-learn, keras, tensorflow, matplotlib
+ Download all of the files linked below and save them to 'bottleneck_features/' : 
    - [VGG-19](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/DogVGG19Data.npz) bottleneck features
    - [ResNet-50](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/DogResnet50Data.npz) bottleneck features
    - [Inception](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/DogInceptionV3Data.npz) bottleneck features
    - [Xception](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/DogXceptionData.npz) bottleneck features

## Project Motivation and approach<a name="motivation"></a>

+ The aim of this project is to build a deep neural network to identify the breed of a dog.
+ We start with training a CNN from scratch without any image augmentation, and then add in image augmentation. This should make for a better model, as augmentation corrects for position and orientation of features in the training images.
+ Training from scratch is time and resource intensive, so instead of further fine-tuning we can use transfer learning to use parts of pre-trained CNNs and fit them on our data to build a model. This should give better results with shorter training times

## File Descriptions <a name="files"></a>

+ dogImages/ : Three folders of dog images for train,validation & test datasets. The images have been provided by Udacity as part of Data Scientist nanodegree.
+ dog-breed-classifier.ipynb : Notebook used to train the various CNNs
+ Saved model/ : For all models trained, weights with the best validation loss are saved here.
+ bottleneck_features/ : Location to save the pre-computed bottleneck features

## Conclusion <a name="Conclusion"></a>

It is clear that transfer learning yields the best results for the shortest training time. Also Image augmentation increases accuracy but also takes much longer to train

## Licensing, Authors, Acknowledgements<a name="licensing"></a>

The datasets were provided by Udacity. Some of the functions used in the code were from the lessons in the Udacity Data Scientist Nanodegree program.
