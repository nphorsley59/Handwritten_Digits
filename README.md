# <div align="center">Digit Recognition</div>

### <div align="center">Project Overview</div>
Computer vision is a common application of machine learning algorithms. I used the MNIST dataset (shared as a Kaggle competition) to demonstrate the application of classification methods (SVM and KNN) and neural networks to computer vision. The primary objective of the project was to train a model to recognize hand-written digits (0-9) in scanned, black-and-white images. For a more in-depth look at this analysis, please refer to my [Jupyter Notebook]().

### <div align="center">Preparation</div>
Preparing the MNIST dataset for analysis was relatively straight-forward. Even though I assumed it was a clean dataset, I ran some quick tests looking for NaNs and other potential typos/outliers to be safe. I also collected some basic information about the structure of the dataset and visualized the images the model would be working with (Figure 1). The full dataset contained 42,000 28x28 images of digits, ranging from 0-9.

**Figure 1.** A gray-scale image of a hand-written '9'.</br>

![alt_text](https://github.com/nphorsley59/Digit_Recognition/blob/master/Figures/digit_9.png "Sample Digit")

### <div align="center">Modeling</div>

#### 1. Support Vector Machine
I was interested in building several different models and comparing their performance. I started with a relatively simple classification method, SVM. There were a few steps to this method: 1) scale the data to have a mean of 0 and a variance of 1, 2) use subsets of the 'train' set as a model-building 'train' and 'test', 3) built and fit the model, and 4) test the accuracy of the model.

#### 2. K-nearest Neighbor
I used another commonly used classification method, K-nearest Neighbor, to group images by digit. 

#### 3. Neural Network

### <div align="center">Resources</div>
https://www.kaggle.com/c/digit-recognizer
