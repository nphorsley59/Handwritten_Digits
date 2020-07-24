# <div align="center">Digit Recognition</div>

### <div align="center">Project Overview</div>
Computer vision is a common application of machine learning algorithms. I used the MNIST dataset (shared as a Kaggle competition) to demonstrate the application of classification methods (SVM and KNN) and neural networks to computer vision. The primary objective of the project was to train a model to recognize hand-written digits (0-9) in scanned, black-and-white images. For a more in-depth look at this analysis, please refer to my [Jupyter Notebook]().

### <div align="center">Preparation</div>
Preparing the MNIST dataset for analysis was relatively straight-forward. Even though I assumed it was a clean dataset, I ran some quick tests looking for NaNs and other potential typos/outliers to be safe. I also collected some basic information about the structure of the dataset and visualized the images the model would be working with (Figure 1). The full dataset contained 42,000 28x28 images of digits, ranging from 0-9.

**Figure 1.** A gray-scale image of a hand-written '9'.</br>

![alt_text](link "Sample Digit")

### <div align="center">Modeling</div>
I was interested in building several different models and comparing their performance. I started with a relatively simple classification method, Support Vector Machine (SVM).

### <div align="center">Resources</div>
https://www.kaggle.com/c/digit-recognizer
