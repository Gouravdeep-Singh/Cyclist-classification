# Cyclist-classification
The aim of our project is to study and analyse the given datatset about Different Cyclist and classify it into categories- casual member or actual member. The datatset has been acquired through kaggle. Our analysis is divided into following steps: 
Knowing the Dataset
Variance Threshold
Time extraction
Recursive feature selection
Visualization
Outlier handling
Model Implementation
Evaluation
It also involves handling of missing values, checking the shape of our dataset, figuring out the datatypes of each feature and also encoding categorical feature to numerical.
In Time extraction we use the datetime model and calculate the time taken for a cyclist to reach their destination and form a new feature based on it.
On visualizing the data using heatmap we try to analyze the correlation among various features. features with low correaltion wil be dropped. Also we check the varriablity using Various Threshold- True indicating high variabilty while false meaning less variablity. we drop the features with low variability to avoid redundancy.
In recursive feature selection, we check the importance of each selected feature with respect to our target uisng random forest algorithm.
The outliers are detected using IQR and were removed using flouring and capping. Log transformation is also used to check for skweness.
For model implemtation we have used Random forest algorithm, logistic regression algorithm and KNN algorithm. To evalute their results confusion matrix and classification report were implemnted.
Our random forest model overfits with a difference of 0.18 between training and testing data, for KNN its 0.10 while logistic regression has it at 0.02
# Observations
Major issue we faced was the size of our dataset. We had to extract time from nearly 7 lakh rows and extracting time difference from even 5000 rows took us three hours, so we decided to limit our dataset upto 10,000 rows.
While evaluating the features we faced contradicting results. The output after variance threshold revealed that most of the features were less variable and logically should be dropped but recursive feature elimination showed that those same features were important for our target column. We decided to drop them to reduce overfitting. 
Out of the three classification algorithms best results were given by Logistic regression model reason being it is best suited for data which is binary and linear.
