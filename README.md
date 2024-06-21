# model-sugar-intake
Building Sugar Intake Recommendation System with Regression Linear using TensorFlow. This notebook provide preprocessing data, training model, and testing the model output to recommending amount of daily sugar intake based on user input in self assessment content.

Notebook Preparation

The notebook that used in the code in this repo is from Google Colabs

We will use pandas library to preprocessing purpose (colect, read, and cleaning data), then we also use sickit-learn library for preproces the data too before train the model. Then we use tensorflow to build model, training the model, and save the model.

Cleaning Dataset

The next thing that we do is to check and cleaning the dataset (checking null input, or duplicate input in dataset), for best training model purpose (avoid overfitting or underfitting). We also divide the two types of data into numerical and categorical.

To check missing value in data, we can use

data = data.dropna()

Preparation Data for Training

First we will get the variable that we want to match and train from user. Then we encode the input variable with OneHotEncoder to be float format. Next the input and target data will be splited to train and test data to training process.

Training Model

Training model will use tensorflow with custom model. From tensorflow library we use model Dense, Adam optimizer for optimizing, and, MSE loss for the training model.

We will use numerical and categorical data as diferent input in the neural network which have independent layer. Then each input will be merged with concatenate process to match each input, so we can get the compatibility of each input that play important role in this recommendation system. Then we can start train the model with model.compile, and model.fit.

Testing Model

In this process, we will repeat the preprocessing step for new input variabel from user (encode the input with OneHotEncoding)

Generate Recommendation

From the new input, we will generate the recommendation model to outputing the best compatibility amount of the daily sugar intake and user input from the model variabel.
