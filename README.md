# Cyclist-classification
# Objective: 
The aim of our project is to study and analyze the given data about Different Cyclists and classify it into categories- casual members or actual members. The data set has been acquired through Kaggle. Our analysis is divided into the following steps: Knowing the Dataset Variance Threshold Time extraction Recursive feature selection Visualization Outlier handling Model Implementation Evaluation Our analysis is divided into the following steps: 
Knowing the Dataset
Variance Threshold
Time extraction
Recursive feature selection
Visualization
Outlier handling
Model Implementation
Evaluation
# EDA: 
It involves handling missing values, checking the shape of our dataset, figuring out the datatypes of each feature and encoding categorical features to numerical using a label encoder. In Time extraction we use the datetime model and calculate the time taken for a cyclist to reach their destination and form a new feature based on it. On visualizing the data using a heatmap we try to analyze the correlation among various features. features with low correlation will be dropped. Also, we check the variability using Various Threshold- True indicates high variability while false means less variability. we drop the features with low variability to avoid redundancy.
# In recursive feature selection, we check the importance of each selected feature with respect to our target using a random forest algorithm.
The outliers were detected using IQR and were removed using flouring and capping. Log transformation is also used to check for skewness. if the skewness of the feature is less than that of a feature when it is log-transformed then we use the original feature else we use the transformed one.
# Model: 
For model implementation we have used the Random forest algorithm, logistic regression algorithm and KNN algorithm. To evaluate their results confusion matrix and classification report were implemented.
Our random forest model overfits with a difference of 0.18 between training and testing data, for KNN it's 0.10 while logistic regression has it at 0.02
# Observations
The major issue we faced was the size of our dataset. We had to extract time from nearly 7 lakh rows and extracting time difference from even 5000 rows took us three hours, so we decided to limit our dataset to 10,000 rows.
While evaluating the features we faced contradicting results. The output after the variance threshold revealed that most of the features were less variable and logically should be dropped but recursive feature elimination showed that those same features were important for our target column. We decided to drop them to reduce overfitting. 
Out of the three classification algorithms best results were given by the Logistic regression model reason being it is best suited for data which is binary and linear.
