## Classifying Music Genres with ANN, tuned ANN, CNN & RNN

The aim of this project is to develop and tune multiclass classification model with deep neural networks that accepts MFCC's as an input and matches it to one of 10 possible genres:

* **preprocessing.py** Loops through music dataset directory, extracts **MFCCs** and saves them into a json file along witgh genre labels

* **ANN_Classifier.py** implements a simple sequantial neural network with 3 hiddel layers, sparse categorical crossentropy loss function and relu+softmax activation function. It then trains, tests and evaluates the model

* **Tuned_ANN_Classifier.py** Takes ANN_Classifier.py and tunes it such that it can generalize better with test set. Specifically, it adds support for ad-hoc neuron **dropout** and **L2 regularization**:

![alt text](https://github.com/paabes/AudioSignal-Deep-Learning/blob/main/Classifying%20Music%20Genre%20With%20ANNs/figures/accuracy_eval.jpg)

* **CNN_Classifier.py** implements Convolutional Neural Network classification model with 3 Convolutional and 2 Dense layers. Specifically, it assumes that the audio signal data is esentially image data, with X-values being 13 Mel-Frequency coefficients and Y-values being individual data points (separate chuncks of audio from which MFCC's have been extracted). input.shape = [100, 13], however, since audio data does not have color depth, input is reshaped to add an extra dimesion of value 1: shape = [100, 13, 1], which, to my srurprise, worked perfectly well and after some tuning the model achieved over 85% accuracy after 300 epochs and batch size of 16:

![alt text](https://github.com/paabes/AudioSignal-Deep-Learning/blob/main/Classifying%20Music%20Genre%20With%20ANNs/figures/CNN_accuracy_eval.jpg)


* **RNN_Classifier.py** Since audio data can be thought of as univariate (in case of waveforms), or multivariate (in case of spectograms) time-series data, and recurrent neural networks are notorious for extracting patterns from sequential data, I thought it would be interesting to see how much of a performance boost we obtaim from the model if we use this approach instead of conventional MLP and CNN's
 

* Dataset is approximately 1.5GBs which is why I have not included it in the repo, it is available for free at: https://www.kaggle.com/andradaolteanu/gtzan-dataset-music-genre-classification
