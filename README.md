# Portfolio

Welcome!

This repository is a collection of projects I did to present my skills.
Each directory contains a .ipynb file where I do and describe all the necessary steps for a particular task. 
In these notebooks I justify the decisions made. All projects were made using google colab. For ploting I used plotly express which produces interactive plots, but
they aren't displayed here so I included them as png. 
Below I'll describe each project in few sentences.

1. Housing price prediction:

    It's a regression task so it's in a folder called regression. I work with dataset found on Kaggle which have information about houses and the price they sold for. 
    My goal is to predict the price they sold for using information included in the dataset. For data manipulation I used numpy and pandas. For training models I used sklearn,
    XGBoost and cuML which basically is sklearn with gpu support. cuML doesn't have all the features sklearn have but it compatible whit sklearn objects. For example 
    scaler in a pipeline might be sklearn object and regressor might be cuML object, as long as model is a cuML object and gpu is avaliable training will be much faster than using sklearn
    
2. Heart disease prediction:

    In this project, I use patients medical information to predict whether they have heart disease or not. It's a binary classification problem and it's located in a directory called Classification.
    I used the same libraries as for the housing price prediction project
    
3. Forecasting average daily temperature in Delhi:

    My goal for this project was to produce 30 day forecast of average temperature so it's a time series forecasting task and it's located in a folder named that way.
    In this project I used numpy and pandas for data manipulation and NeuralProphet for forecasting. Some of the functionalities that I wanted to use are built into NeuralProphet but they are done in a way that doesn't suit me.
    I wrote a wrapper function that used built in functionalies of NeuralProphet, this function does crossvalidation and plots forecasts against ground truth data in a way that suits me.
    
4. Named entity recognition:

    Named entity recognition is a task of classyfying each word as one of named entities. It's a Natural Language Processing task and modern NLP world is dominated by 
    Transformers based models which are a specific type of neural network architecture. I used Huggingface's transformers library that offers pretrained implementations 
    of modern transformers based models. I tracked my experiments with Weights&Biases. 
    
5. Summarization of short conversations





















