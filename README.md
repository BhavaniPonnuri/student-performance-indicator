## End to End Data Science and Machine Learning Project

**The Goal of this project is to predict the student score based on the data and indicate their performance**

#### Introduction to data:
Input Features:
* gender, race_ethnicity, parental_level_of_education, lunch, test_preparation_course, reading_score, writing_score

Target Feature:
* maths_score

## Approach for the Project:

1. Data Ingestion : 
    * In Data Ingestion phase the dataset is first read as csv. 
    * Then the data is split into training and testing and saved as csv files.

2. Data Transformation : 
    * In this phase a Column Transformer is created which combines two different pipelines.
    * For the numerical features, a pipeline is created with SimpleImputer to handle Outliers, scale the data using StandardScaler.
    * For the categorical features, a pipeline is created with SimpleImputer to handle Outliers, OnehotEncoder to encode the features into numerical data and finally scale the data using StandardScaler.
    * This preprocessor is saved as pickle file.

3. Model Training : 
    * In this phase base model is tested on different machine learning regression algorithms such as LinearRegression, DecisionTreeRegressor, KNeighborsRegressor, XGBRegressor, AdaBoostRegressor, GradientBoostingRegressor, RandomForestRegressor,CatboostRegressor. The best model found was CatboostRegressor.
    * After this hyperparameter tuning is performed on Decision Tree, Gradient Boosting Regressor, Random Forest Regressor, XGB Regressor, AdaBoost Regressor, Catboost Regressor.
    * A final model is created with the CatboostRegressor.
    * This model is saved as pickle file.

4. Prediction Pipeline : 
    * This pipeline converts given data into dataframe and has various functions to load pickle files and predict the final results in python.

5. Flask App creation : 
    * Flask app is created with User Interface to predict the gemstone prices inside a Web Application.
