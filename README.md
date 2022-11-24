# Portfolio

Welcome!

This repository is a collection of projects I created to present my skills.
Each directory contains a .ipynb file where I perform and describe all the necessary steps to complete a particular task. 
In these notebooks I describe the justifications for my decisions. All projects were made using Google colab. For plotting I used Plotly which produces interactive plots, but
they aren't displayed here so I included them as a png. 
Below I'll describe each project in a few sentences.

1. Housing price prediction:

    It's in a folder called Regression because it's a regression task. I work with a dataset found on Kaggle that have information about houses and the price they were sold for. 
    My goal is to predict the price they were sold for using information included in the dataset. For data manipulation I used NumPy and Pandas. For training models I used sklearn,
    XGBoost and cuML which basically is sklearn with GPU support. cuML doesn't have all the features sklearn has but it is compatible whit sklearn objects. For example 
    a scaler in a pipeline might be a sklearn object and a regressor might be a cuML object, as long as the model is a cuML object and if a GPU is available training will be much faster than when using sklearn.
    
2. Heart disease prediction:

    In this project, I used patients medical information to predict whether they have heart disease or not. It's a binary classification problem and it's located in a directory called Classification.
    I used the same libraries as for the housing price prediction project
    
3. Forecasting average daily temperature in Delhi:

    My goal for this project was to produce a 30 day forecast of average temperature so it's a time series forecasting task and it's located in a folder named Time Series Forecasting.
    In this project I used numpy and pandas for data manipulation and NeuralProphet for forecasting. Some of the functionalities that I wanted to use are built into NeuralProphet but they are done in a way that doesn't suit me.
    I wrote a wrapper function that used the built-in functionalies of NeuralProphet, this function does cross-validation and plots forecasts against ground truth data in a way that suits me.
    
4. Named entity recognition:

    Named entity recognition is a task that classifies each word as one of several named entities. It's a Natural Language Processing task and the modern NLP world is dominated by 
    Transformers based models which are a specific type of neural network architecture. I used Huggingface's Transformers library that offers pre-trained implementations 
    of modern Transformers based models. I tracked my experiments with Weights&Biases. 
    
5. Summarization of short messenger like conversations:

    Summarization is also an NLP task and I used the same liblaries as for NER project. My goal wasn't to train a perfect production ready model but to show that I'm capable of training a model for such a task.
    
6. Question Answering:

    Question answering is another NLP task. I trained models to perform Extractive Question Answering which means that given a passage and question regarding that passage a part of passage is returned as an answer. I used the same libraries as for NER and Summarization projects. Difference between this project and 2 previous ones is that I used TensorFlow for training instead of Transformer's Trainer.





















