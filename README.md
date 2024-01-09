DESCRIPTION
=================================================================================================================================
This project is to classify wine quality based on several factors included in the wine quality dataset. 
<br>The dataset was obtained from UC Irvine Machine Learning Repository. Before the model was trained, the data underwent several steps, such as data preprocessing and exploratory data analysis. 
<br>These processes include data visualization, data cleaning, feature engineering, splitting data, data oversampling, and so on.
 
The model that was used as the final classifier is XGBoost, which was chosen because it performed better compared to several other machine learning models. 
<br>After the comparison, the XGBoost model's performance was further improved by using hyperparameter tuning. As this project was made for college project purposes, no further deployment was done.


RELATED FIELDS
=================================================================================================================================
Data Analysis | Data Visualization | Data preprocessing & cleaning 
<br>Machine Learning | Classification | Boosted Algorithm | Parameter Tuning


DATASETS
=================================================================================================================================
The dataset was obtained from the following link:
<br>https://archive.ics.uci.edu/dataset/186/wine+quality
<br>Some examples of the independent variables are:
- fixed acidity
- volatile acidity
- residual sugar
- chlorides
- density
- sulphates, etc.
  
<br>There are 4898 rows in this dataset.


Exploratory Data Analysis Conclusion
=================================================================================================================================
After further EDA process, my analysis is concluded into several points, which are as follows:
- There is an extreme class imbalance, so the oversampling method will be performed during data preprocessing.
- No independent variable has a strong correlation with the target variable. For example, ‘Alcohol’ level with a 43.55% correlation score is the one with the highest correlation score.
- Multiple multi-colinearities are detected from the analysis. Like residual sugar and density (83.89%) and free sulfur dioxide and total sulfur dioxide (61.55%).
- Quite a lot of data are considered outliers when boxplot visualization is performed.


PREPROCESSING
=================================================================================================================================
Multiple preprocessing steps are performed for the dataset, which includes:
1) Feature Engineering
2) Outliers Removal (Using Z-Score Filtering)
3) Oversampling (Using SMOTE Algorithm)
4) Standardization (By StandardScaler)


MODELLING EVALUATION
=================================================================================================================================
After comparing multiple machine learning models, here are the result:
No | Model | Accuracy | Precision | Recall | F1-score |
--- | --- | --- | --- |--- |--- |
0	|Decision Tree	|0.566999	|0.594079	|0.566999	|0.576733
1	|RandomForest	|0.655592	|0.656794	|0.655592	|0.655646
2	|XGBoost	|0.673311	|0.670562	|0.673311	|0.669137
3	|LogisticRegression	|0.349945	|0.472822	|0.349945	|0.375686
4	|CatBoost	|0.625692	|0.626649	|0.625692	|0.625857
5	|LGBM	|0.627907	|0.630481	|0.627907	|0.627359
6	|KNN	|0.495017	|0.560663	|0.495017	|0.512409
7	|ADA	|0.306755	|0.438135	|0.306755	|0.331874
