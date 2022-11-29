Welcome!

In this project I predict whenether patient has a heart disease or not basing on patient's medical information. 
Dataset I'm working has 918 rows, 508 rows labeled as class 1 meaning that patient has a heart disease and 410 rows labeld as class 0.
First I do exploratory data analysis and then data cleaning. During EDA I found some missing values. I decided to impute these missing values with Iterative Imputer from Scikit-Learn. Iterative Imputer trains a machine learning algorithm on rows with complete data to predict and impute values for rows with missing values.

I trained various machine learning algorithms and compared them with each other. Metric that decided the best model was Recall of class 1, it takes into account situations where patient had a heart disease but was classified as a healthy person which is a worst case scenario.

To find optimal paremeters for each algorithm I used GridSearch with 5 fold cross-valitation. To avoid data leakage scaler (if necessary) and imputer are packed together with a classifier using Pipeline, all objects inside of this pipeline are refitted every validation fold with available data. 
