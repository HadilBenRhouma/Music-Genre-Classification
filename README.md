README FILE: A good project idea is to build a model that can classify the genre of music using neural networks. We would need to extract information from the audio samples such as spectrograms, MFCC, etc. and then use a model to classify the music genre. This model can be used to automatically classify the music genre.

Music Genre Classification – Automatically classify different musical genres:
In this tutorial we are going to develop a deep learning project to automatically classify different musical genres from audio files. We will classify these audio files using their low-level features of frequency and time domain.
For this project we need a dataset of audio tracks having similar size and similar frequency range. GTZAN genre classification dataset is the most recommended dataset for the music genre classification project and it was collected for this task only.

About the dataset:
The GTZAN genre collection dataset was collected in 2000-2001. It consists of 1000 audio files each having 30 seconds duration. There are 10 classes ( 10 music genres) each containing 100 audio tracks. Each track is in .wav format. It contains audio files of the following 10 genres:
- Blues
- Classical
- Country
- Disco
- Hiphop
- Jazz
- Metal
- Pop
- Reggae
- Rock

There are various methods to perform classification on this dataset. Some of these approaches are:
Multiclass support vector machines
K-means clustering
K-nearest neighbors
Convolutional neural networks

We will use K-nearest neighbors algorithm because in various researches it has shown the best results for this problem.
K-Nearest Neighbors is a popular machine learning algorithm for regression and classification. It makes predictions on data points based on their similarity 
measures i.e distance between them.

Steps to build Music Genre Classification:
1. Imports
2. Define a function to get the distance between feature vectors and find neighbors
3. Identify the nearest neighbors
4. Define a function for model evaluation
5. Extract features from the dataset and dump these features into a binary .dat file “my.dat”
6. Train and test split on the dataset
7. Make prediction using KNN and get the accuracy on test data
