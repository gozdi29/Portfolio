# Portfolio

Welcome!

This repository is a collection of projects I created to present my skills.
Each directory contains a .ipynb file where I perform and describe all the necessary steps to complete a particular task. 
In these notebooks I describe the justifications for my decisions. For plotting I used Plotly which produces interactive plots, but
they aren't displayed here so I included them as a png. 
Below I'll describe each project in a few sentences.

   
1. Heart disease prediction (Classification directory):
    
    In this project I predict whenether a patient has heart disease based on their medical information. 
    Initially I made this project on Google Colab where I used cuML and XGBoost for model training, Pandas and NumPy for data manipulations. I searched for optimal hyperparameters using GridSearchCV. 
    
    After a while I wanted to learn Spark and I came across Databricks. Using the same dataset I remade this project using PySpark for data manipulation, Spark's MLLIb for model training, Hyperopt for hyperparameter search and MLFlow for experiment tracking and model registery.
    
    I have also made a simple app for inference using FastAPI and Dockerized it for deployment. I was planning to deploy it on Heroku that's why it is also in a separate repository. I'm currently looking for a free alternative to Heroku, which is no longer free, to deploy the app.
    
    
2. Forecasting average daily temperature in Delhi:

    My goal for this project was to produce a 30 day forecast of average temperature so it's a time series forecasting task and it's located in a folder named Time Series Forecasting.
    In this project I used NumPy and Pandas for data manipulation and NeuralProphet for forecasting. Some of the functionalities that I wanted to use are built into NeuralProphet but they are done in a way that doesn't suit me.
    I wrote a wrapper function that extended the built-in functionalies of NeuralProphet, this function does cross-validation and plots forecasts against ground truth data using interactive Plotly plots instead of static matplotlib.
    
3. Named entity recognition:

    Named entity recognition is a task that classifies each word as one of several named entities. Modern NLP world is dominated by 
    Transformer based models which are a specific type of neural network architecture. I used Huggingface's Transformers library that offers pre-trained implementations of state of the art models. Besides showing my ability to fine-tune a model for NER task I wanted to test if DeBERTAv3 xSmall with a backbone of only 22M parameters can outperform RoBERTa base which has 86M backone parameters. I've chosen these specific models because in DeBERTav3 paper autors claim that xSmall variant of their model can outperform RoBERTa base variant on some tasks. I tracked my experiments with Weights&Biases which allowed me to do a comprehensive comparison of metrics they achieved and also their performance during training. Thanks to Huggingface, inference API is avaliable here https://huggingface.co/Gozdi/roberta-base-finetuned-ner
    
4. Summarization of short messenger like conversations:
    
    In this project I fine-tune one of T5-efficient variants on Samsum dataset to do abstractive summarization. Samsum is a dataset composed of short messenger like conversations written by linguists fluent in English. T5-efficient is a collections of augmented T5 models that were developed during a study of efficient scaling of transformers. I picked a variant that is small but has good metrics and outperforms other variants with comparable number of parameters. I tracked my experiments with Weights&Biases. Summaries generated by model fine-tuned by me sometimes are far from perfect but training a perfect model wasn't my goal. My goal was to show my ability and necessary knowledge for fine-tuning Transformer Encoder-Decoder model for text generation task such as summarization or translation.
    
    Inference API is avaliable here https://huggingface.co/Gozdi/t5-efficient-small-nl16-samsum-exp2. 
    
    Here's also an example conversation:
    
    Oscar: A coffee at Tristano's?

    Payne: Why not. in 15 mins?

    Oscar: let's make it half an hour ok?

    Payne: great, i'll be there

    Oscar: see you there
    
    
5. Question Answering:

    In this project I fine-tuned different Transformer based models on AdversarialQA dataset to do extractive question answering, which means that given a passage and question regarding that passage, a part of the passage is returned as an answer. AdversarialQA dataset was construced using 3 models fine-tuned on SQuAD dataset, these models were DiBAF, BERT and RoBERTa. Humans were paid to come up with questions regarding SQuAD passages and if trained model wasn't abel to answer them correctly they were added to the dataset. I fine-tuned couple of different models on this dataset and later I fine-tuned the one with the best performance on AdversarialQA and SQuAD. Fine-tuning on these 2 datasets improved performance on AdversarialQA. This was one of my first NLP projects and at that time I didn't know how great Weights&Biases is so I didn't use it for experiment tracking. I was tracking models metrics using Pandas dataframes which now doesn't seems like a good idea.
    
    Inference API is avaliable here https://huggingface.co/Gozdi/Electra-base-squad-adversarialqa-epoch-3
    
