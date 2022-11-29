Welcome!

In this project I predict prices of properties basing on it's attributes.

My first step was to explore and visualize the data. During this process I gained information that allowed me to engineer new features, get rid of or fix some of the exisiting
ones. I've also tried to detect and delete outlying samples. I classified samples as outliers if discrepancy between price percentile and percentiles of some of the most correlated with price columns was big.
By big discrepancy I mean when price is in 90th percentile and 2 most correleated features are belowe their's 60th percentiles.

One of the features I engineered was 'neighbourhood cluster' which I got clustering samples into 20 categories with K-means algorithm using their geographical coordinates. I used it for Linear Regression.

After data exploration and cleaning I trained Linear Regression and XGBRegressor and performed error analysis. After error analysis I concluded that either of the models isn't capable of 
accurately predicting for houses with price over 1.4m so I decided to drop these rows.

Finally I trained different types of models and chose the best one using RMSE. I tried to find optimal parameters for each of the models with 5 fold cross-validation GridSearch.

Main goal of this project was to demonstrate knowledge of all the necessary steps and insights for performing regression with ML algorithms.
