# Image-classification-using-deep-learning
Classifying different classes in images with the help of deep knowledge

This code pattern demonstrates how images, specifically document images like buildings, forest, sea, glacier can be classified using Convolutional Neural Network (CNN).


## What is CNN and why CNN? 
A CNN is a supervised learning technique which needs both input data and target output data to be supplied. These are classified by using their labels in order to provide a learned model for future data analysis.

CNN has three main constituents - a Convolutional Layer, a Pooling Layer and a Fully connected Dense Network. 
The Convolutional layer takes the input image and applies m number of nxn filters to receive a feature map. 
The feature map is next fed into the max pool layer which is essentially used for dimensionality reduction, it picks only the best features from the feature map. 
Finally, all the features are flattened and sent as input to the fully connected dense neural network which learns the weights using backpropagation and provides the classification output.

The **MOTIVATION** behind the CNN is that it takes one section/window of the input image at a time for classification. Each time the CNN will produce a feature map for each section, in the convolutional layer. 
In the Pooling layer it removes the excess features and takes only the most important features for that section, thereby performing feature extraction.  
Hence, with the use of CNNs we don't have to perform an additional feature extraction technique.
CNNs require lesser pre-processing as compared to other similar classification algorithms.

## Getting Started
Use the Anaconda navigator to open the Jupyter notebook and start implementing it.

## Pre-requisites 

**Install all these libraries in your local environment**
* Numpy
* Pandas
* Scikit-learn
* Keras
* cv2
* pathlib
* glob
* os

### Dataset
This is image data of Natural Scenes around the world.
This Data contains around 25k images of size 150x150 distributed under 6 categories. {buildings, forest, glacier, mountain, sea,  street}
There are around 14k images in Train, 3k in Test and 7k in Prediction.

## Working
- Firstly, I imported all the useful libraries needed for our project. Then we started by creating empty lists for our training data, test data folder. 
- After all this, get all the images from directories to predefined empty lists, by reading them and resizing them so that all the images are of same size. After this, start making the model and training the data. 
- The main **challenge** in making the model to create a efficient one which has low computational cost. By using the separable convolution instead of traditional convolution layer we achieved the better result with less computation cost.

## Acknowledgement
Used the dataset from kaggle [intel-image-classification](https://www.kaggle.com/puneet6060/intel-image-classification) .
Thanks to https://datahack.analyticsvidhya.com for the challenge and Intel for the Data.
Photo by Jan Böttinger on Unsplash
