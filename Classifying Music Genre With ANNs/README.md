## Classifying Music Genres with ANN, tuned ANN, CNN & RNN

The aim of this project is to develop and tune multiclass classification model with deep neural networks that accepts MFCC's as an input and matches it to one of 10 possible genres:

* **preprocessing.py** Loops through music dataset directory, extracts **MFCCs** and saves them into a json file along witgh genre labels
* **ANN_Classifier.py** implements a simple sequantial neural network with 3 hiddel layers, sparse categorical crossentropy loss function and relu+softmax activation function. It then trains, tests and evaluates the model
* **Tuned_ANN_Classifier.py** Takes ANN_Classifier.py and tunes it such that it can generalize better with test set. Specifically, it adds support for ad-hoc neuron **dropout** and **L2 regularization**:

![alt text](https://github.com/paabes/AudioSignal-Deep-Learning/blob/main/Classifying%20Music%20Genre%20With%20ANNs/figures/accuracy_eval.jpg)
 
* Dataset is approximately 1.5GBs which is why I have not included it in the repo, it is available for free at: https://www.kaggle.com/andradaolteanu/gtzan-dataset-music-genre-classification