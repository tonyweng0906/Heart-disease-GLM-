Heart Disease Prediction - Statistical Analysis Project
📊 Project Overview
This project presents a comprehensive statistical analysis of heart disease prediction using clinical data from Kaggle. The study employs Generalized Linear Models (GLMs) with logit, probit, and complementary log-log links to identify key risk factors and build predictive models for heart disease probability.

🎯 Research Objectives
Identify Key Risk Factors: Determine which clinical features significantly impact the probability of developing heart disease

Quantify Impact Magnitude: Assess how and to what extent these factors influence disease probability

Develop Predictive Models: Build statistical models to predict individual heart disease risk

📁 Dataset Description
Source: Kaggle Heart Failure Prediction Dataset (fedesoriano, September 2021)

Size: 918 observations with no missing values or duplicate rows

Variables:

Response: HeartDisease (binary: 1 = Heart Disease, 0 = Normal)

11 Clinical Predictors: Age, Sex, ChestPainType, RestingBP, Cholesterol, FastingBS, RestingECG, MaxHR, ExerciseAngina, Oldpeak, ST_Slope

🔬 Methodology
Exploratory Data Analysis
Numerical summaries and distribution visualizations

Correlation analysis between variables

Comparative analysis of categorical vs. continuous predictors

Statistical Modeling
Sequential Log-Likelihood Ratio Tests for variable selection

Three Link Functions Tested:

Logit (logistic regression)

Probit (normal CDF)

Complementary Log-log (extreme value distribution)

Model Diagnostics:

Pearson chi-squared tests

Hosmer-Lemeshow goodness-of-fit test

AIC/BIC for model comparison

Key Results
Best Logit Model: Excludes RestingECG, RestingBP, MaxHR, and Age

Best Probit Model: Excludes RestingECG, RestingBP, and MaxHR

Best Cloglog Model: Excludes RestingECG, Age, RestingBP, MaxHR

📈 Key Findings
Significant Predictors
Strong Positive Association:

Male sex (OR = 4.28 in logit model)

Exercise-induced angina (OR = 2.69)

Flat ST slope (OR = 4.23 vs. downsloping)

Strong Negative Association:

Cholesterol levels (higher reduces risk)

Atypical chest pain types (ATA/NAP/TA)

Model Performance
Probit Model: Lowest deviance (596.27) and AIC (620.27)

Logit Model: Lowest BIC (674.65), most interpretable

Cloglog Model: Slightly worse performance but viable

Goodness-of-Fit
All models passed diagnostic tests:

Pearson chi-square: p > 0.05 for all models

Hosmer-Lemeshow: p > 0.05 for all models

No significant evidence of model misfit

🛠️ Technical Implementation
Tools & Libraries
R Programming Language

Key Libraries:

ggplot2, ggpubr for visualization

corrplot for correlation analysis

dplyr for data manipulation

Base R statistical functions

Code Structure
Data Loading and Cleaning

Exploratory Data Analysis

Model Building and Selection

Diagnostics and Validation

Interpretation and Visualization

📋 How to Reproduce
Prerequisites
R (≥ 4.0.0)

RStudio (recommended)

Required R packages (see Rmd file for list)

Steps
Clone/download the project files

Ensure heart.csv is in the working directory

Open MATH 6622 Project.Rmd in RStudio

Install required packages if missing

Knit the Rmd file to generate PDF/HTML report

📄 Output
The analysis generates:

Comprehensive statistical report (PDF/HTML)

Visualizations of distributions and relationships

Model comparison tables

Odds ratios with confidence intervals

📚 References
Dataset: fedesoriano. (September 2021). Heart Failure Prediction Dataset. Retrieved from https://www.kaggle.com/fedesoriano/heart-failure-prediction

Methodology: Agresti, A. (2013). Categorical Data Analysis (3rd ed.). Wiley.

GLM Theory: McCullagh, P., & Nelder, J. A. (1989). Generalized Linear Models (2nd ed.). Chapman & Hall.

👥 Authors
Statistical Analysis Project - MATH 6622 Course

📄 License
This project is for academic purposes. Dataset usage should comply with Kaggle's terms of service.
