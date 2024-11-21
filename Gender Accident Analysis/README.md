# Gender-Specific Car Crash Analysis

### Project Overview
This project focuses on analyzing a road traffic accident dataset to explore the relationship between driver gender and accident type/severity. Using machine learning techniques, the analysis aims to classify the gender of the driver based on various features such as accident conditions, driver characteristics, and environmental factors.

### Dataset Description
The dataset, RTA_dataset, was sourced from Kaggle and contains detailed information on road traffic accidents, including:

1. Driver Information: Age, gender, educational level, driving experience.
2. Accident Context: Severity, cause, type of collision, road surface type, weather, light conditions.
3. Other Variables: Pedestrian movement, vehicle movement, and lane/median type.

## Key Features:
1. Sex_of_driver: Target variable for classification.
2. Accident_severity: Severity of the accident (Slight, Serious, Fatal).
3. Cause_of_accident, Light_conditions, Weather_conditions, and others provide context to accidents.

## Project Goals
Perform exploratory data analysis (EDA) to understand the dataset structure and identify patterns.
Predict the gender of the driver involved in the accident using machine learning models.
Evaluate and compare model performance to determine the most effective approach.
Identify key factors influencing accident severity and gender-based patterns.

#### Data Preprocessing
Steps Taken:

1. Data Cleaning:

Removed rows with missing values to ensure data quality.
Encoded categorical features using Label Encoding to prepare the data for machine learning models.
Exploratory Data Analysis:

2. Generated cross-tabulations to summarize accident severity by gender.
Created bar plots to visualize relationships between features (e.g., severity vs. age group).
Used a correlation matrix and heatmap to identify relationships between variables.
Feature Engineering:

3. Selected relevant features based on correlation analysis for model building.
Machine Learning Models

4. Three models were trained and evaluated:

a. Logistic Regression:

Chosen for its interpretability and effectiveness in binary classification.
Achieved high accuracy (92.8%) on the testing set.

b. K-Nearest Neighbors (KNN):

Hyperparameter tuning (K=11) was performed using GridSearchCV.
Also achieved 92.8% accuracy.

c. Multinomial Naive Bayes:

Well-suited for handling categorical data.
Accuracy: 92.7%, with a slight drop compared to other models.
Performance Metrics:
Accuracy: All models achieved high accuracy on both training and testing sets.
Fairness: Ensured the models perform reasonably well for the minority class (female drivers) using precision, recall, and F1-score.

## Key Findings
Gender and Accident Severity:

Both male and female drivers showed similar severity distributions, with slight injuries being the most common.
Younger drivers (<30 years) accounted for most accidents.

## Influential Features:

Key predictors of gender include Type of Collision, Light Conditions, and Pedestrian Movement.
Features like Educational Level had minimal impact on predictions.

## Class Imbalance:

Female drivers represented only ~5% of the dataset. Additional metrics were used to assess model performance for this underrepresented group.

## Files in the Project
RTA_dataset.csv: The raw dataset used for analysis.
gender_crash_analysis.ipynb: Jupyter Notebook containing all preprocessing, analysis, and modeling steps.

Future Work
1. Additional Models: Explore advanced algorithms like Random Forest or Gradient Boosting for improved predictions.
2. Resampling Techniques: Use SMOTE or similar methods to address class imbalance.
3. Feature Expansion: Include external data (e.g., traffic density or speed limits) for more robust predictions.
4. Deployment: Build a web application to predict driver gender and accident severity based on user inputs.