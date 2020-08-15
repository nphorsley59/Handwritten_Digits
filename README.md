# <div align="center">MNIST Digit Recognition</div>

### <div align="center">Project Overview</div>
Computer vision is a common application of machine learning algorithms. I used the MNIST dataset (shared as a Kaggle competition) to demonstrate the application of classification methods (SVM and KNN) and neural networks to computer vision. The primary objective of the project was to train a model to recognize hand-written digits (0-9) in scanned, black-and-white images. For a more in-depth look at this analysis, please refer to my [Jupyter Notebook]().

### <div align="center">Preparation</div>
Preparing the MNIST dataset for analysis was relatively straight-forward. Even though I assumed it was a clean dataset, I ran some quick tests looking for NaNs and other potential typos/outliers to be safe. I also collected some basic information about the structure of the dataset and visualized the images the model would be working with (Figure 1). The full dataset contained 42,000 28x28 images of digits, ranging from 0-9.

**Figure 1.** A gray-scale image of a hand-written '9'.</br>

![alt_text](https://github.com/nphorsley59/Digit_Recognition/blob/master/Figures/digit_9.png "Sample Digit")

### <div align="center">Modeling</div>

#### 1. Support Vector Machine
I was interested in building several different models and comparing their performance. I started with a relatively simple classification method, SVM. There were a few steps to this method: 1) shuffle the 'train' rows, 2) split 'train' into a Train and Test sets, 3) scale the Train set, 4) build and fit an SVM model, 5) test the accuracy of the model, and 6) identify strengths and weaknesses of the method.

**Figure 2.** Fitting and scoring an SVM model and visualizing its confusion matrix.</br>

![alt_text](https://github.com/nphorsley59/Digit_Recognition/blob/master/Figures/SVM_1.png "SVM Model")</br>

The SVM model tested surprisingly well. Most digits were identified correctly (the numbers on the diagonal). However, the model did struggle to identify 8's and often misidentified digits as 2's. It also only had about 95% accuracy; good but not great.</br>

#### 2. K-nearest Neighbors
A K-nearest Neighbors (KNN) classifier is another commonly used machine learning algorithm.  

**Figure 3.**</br>

#### 3. Neural Network
More advanced machine learning methods, such as neural networks, were not something I had much experience with before this project. I thought this project would be a great opportunity to attempt to build a simple neural network model. The dataset is well-established and I could compare my results with other methods.

**Figure 4.**</br>

### <div align="center">Resources</div>
https://www.kaggle.com/c/digit-recognizer<br/>
https://www.oreilly.com/library/view/hands-on-machine-learning/9781492032632/
