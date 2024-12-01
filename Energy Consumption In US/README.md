
# **Predicting Building Energy Consumption**

## **Project Overview**
This project investigates the key factors influencing energy consumption in buildings across the United States. We aim to develop a predictive model that can forecast future energy consumption based on building characteristics. The analysis uses data from the 2018 Commercial Buildings Energy Consumption Survey (CBECS), which provides detailed information on energy usage and building characteristics of over 6,000 commercial buildings.

The primary goal is to identify significant predictors of energy consumption and create a statistical model to accurately estimate electricity consumption based on these factors.

## **Project Team**
- **Gunj Chinbat** (44197462) – Project Description, Final Editing
- **Niyati Niyati** (47943319) – Data Description & Survey Methodology
- **Parinya Sodsai** (47518723) – Exploratory Data Analysis
- **Jiyoon Kim** (47518723) – Data Cleaning and Transformation
- **Nhu Duong** (48040622) – Regression Analysis

## **Dataset Overview**
The data for this project comes from the **2018 Commercial Buildings Energy Consumption Survey (CBECS)**, which contains detailed information on energy use, building size, and other characteristics of commercial buildings in the United States. The dataset consists of 6,436 records, each representing a single building. The key variables selected for analysis include:

- **ELCNS**: Total electricity consumption (kWh)
- **CENDIV**: Census Division
- **REGION**: Geographic region (Northeast, Midwest, South, West)
- **SQFT**: Total building size in square feet
- **FINALWT**: Final weight to adjust for survey design

## **Survey Methodology**
The dataset is based on a multi-stage area probability sampling method that aims to represent the population of approximately 5.9 million commercial buildings in the U.S. The sampling process includes the use of both area and list frames to ensure adequate representation of various building sizes and regions. Adjustments are made for nonresponse and to maintain the sample's representativeness.

### **Sampling Design**
- **Primary Sampling Units (PSUs)**: 687 counties or groups of counties in the U.S.
- **Secondary Sampling Units (SSUs)**: 8,559 census tracts from which 764 SSUs were sampled.
- **Weighting**: Final weights adjust for nonresponse bias and ensure statistical validity.

## **Data Preprocessing**
- **Log Transformation**: Both the total electricity consumption (ELCNS) and building size (SQFT) variables were log-transformed to improve normality and meet model assumptions.
- **Missing Data**: Missing values in the ELCNS variable were handled through weighted median imputation based on the geographic division (CENDIV).
- **Geographic Analysis**: Geographic variables (REGION and CENDIV) were analyzed to understand regional differences in energy consumption patterns.

## **Regression Analysis**
A forward stepwise regression analysis was conducted to develop the predictive model. The model selection used AIC (Akaike Information Criterion) as the metric for model comparison. The final model, with log-transformed electricity consumption, log-transformed square footage, and CENDIV as predictors, provided the best fit.

### **Key Findings**
- There is a strong positive correlation between building size (SQFT) and energy consumption (ELCNS).
- Geographic location, as represented by the census division (CENDIV), is also a significant predictor of energy consumption.
- The model performed well in diagnostic checks, indicating that it can be used for accurate predictions of energy consumption.

## **Future Research**
Future research could focus on the following areas to improve the accuracy of the energy consumption model:
- Incorporating additional variables such as occupancy patterns, HVAC system types, insulation quality, and renewable energy integration.
- Exploring the temporal dynamics of energy consumption, including seasonal variation and the impact of energy policies.
- Applying advanced machine learning techniques to model complex, non-linear relationships.

## **References**
- U.S. Energy Information Administration. (n.d.). *Commercial Buildings Energy Consumption Survey (CBECS)*. Retrieved from [https://www.eia.gov/consumption/commercial/data/2018/index.php?view=microdata](https://www.eia.gov/consumption/commercial/data/2018/index.php?view=microdata)

## **Appendix**
Additional data visualizations, model diagnostics, and code can be found in the appendices of this report.
