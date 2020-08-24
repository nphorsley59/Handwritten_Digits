# <div align="center">MNIST Digit Recognition</div>

### <div align="center">Project Overview</div>
Skills Demonstrated: *classification algorithms, big data, model optimization, data augmentation*<br />
Libraries and Programs: *Python, Jupyter Notebook, matplotlib, numpy, pandas, scikit-learn, scipy, statistics*<br />

Computer vision is a common application of machine learning algorithms. I used the MNIST dataset to demonstrate the application of classification methods (SVM and KNN) to computer vision. The primary objective of the project was to train a model to recognize digital, black-and-white images of hand-written digits (0-9). My top model correctly classified >97% of the images in the 'test' dataset. For a more in-depth look at this analysis, please refer to my [Jupyter Notebook]().

### <div align="center">Preparation</div>
Preparing the MNIST dataset for analysis was relatively straight-forward. Even though I assumed it was a clean dataset, I ran some quick tests looking for NaNs and other potential typos/outliers to be safe. I also collected some basic information about the structure of the dataset and visualized the images the model would be working with (Figure 1). The full dataset contained 42,000 28x28 images of digits, ranging from 0-9.

**Figure 1.** A sample of hand-written digits from the dataset.</br>

![alt_text](https://github.com/nphorsley59/MNIST_Digit_Recognition/blob/master/Figures/60_digits.png "Sample Digit")

### <div align="center">Modeling</div>

#### 1. Support Vector Machine
I was interested in building several different models and comparing their performance. I started with a relatively simple classification method, SVM. There were a few steps to this method:</br>
1) shuffle the 'train' rows</br>
2) split 'train' into Train and Test sets</br>
3) scale the Train set</br>
4) build and fit an SVM model</br>
5) test the accuracy of the model</br>
6) identify strengths and weaknesses of the method</br>

**Figure 2.** Fitting and scoring an SVM model and visualizing its confusion matrix.</br>

![alt_text](https://github.com/nphorsley59/Digit_Recognition/blob/master/Figures/SVM_1.png "SVM Model")</br>

The SVM model tested surprisingly well. Most digits were identified correctly (the numbers on the diagonal). However, the model did struggle to identify 8's and often misidentified digits as 2's. It also only had about 95% accuracy; good but not great.</br>

#### 2. K-nearest Neighbors
A K-nearest Neighbors (KNN) classifier is another commonly used machine learning algorithm. Similar to SVM, I split this analysis into several steps:</br>
1) shuffle the 'train' rows</br> 
2) split 'train' into Train and Test sets</br>
3) build and fit a KNN model</br>
4) use a grid search to hone the hyperparameters</br>
5) test the accuracy of the model</br>

The base KNN model slightly outperformed the SVM model I tested, but it could be improved. I performed a grid search to find better hyperparameter values.</br>

**Figure 3.** Executing a grid search to compare hyperparameters.</br>

![alt_text](https://github.com/nphorsley59/MNIST_Digit_Recognition/blob/master/Figures/GridSearch.png "KNN Grid Search")</br>

**Figure 4.** Fitting and scoring an adjusted KNN model.</br>

![alt_text](https://github.com/nphorsley59/MNIST_Digit_Recognition/blob/master/Figures/KNN_adj.png "Adjusted KNN Model")</br>

The adjusted KNN algorithm yielded an average cross-validation score of 97%, improving the image recognition accuracy of the model by 2%. For fun, I tried getting even closer to 100% accuracy with data augmentation.</br>

Data augmentation increases the effective sample size of a dataset without actually collecting more data. In this case, I shifted each digit up, down, left, and right, resulting in a training dataset that was 5x larger and had slightly more variation. This model took hours to run and compared almost 200,000 images, roughly 150 million data points. If I had more computing power, I could have added rotated images to the dataset as well.</br>

**Figure 5.** Original and shifted copies of a sample '2'.</br>

![alt_text](https://github.com/nphorsley59/MNIST_Digit_Recognition/blob/master/Figures/shifted_digits.png "Original and Shifted Digits")</br>

**Figure 6.** Model performance for cross-validation of the augmented 'train' dataset.</br>

![alt_text]()</br>

**Figure 7.** Top model performance on the 'test' dataset.</br>

![alt_text]()</br>

### <div align="center">Resources</div>
https://www.kaggle.com/c/digit-recognizer<br/>
https://www.oreilly.com/library/view/hands-on-machine-learning/9781492032632/
