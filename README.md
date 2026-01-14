# Heart Disease Prediction - Statistical Analysis

## 📊 Project Overview
This project presents a comprehensive statistical analysis of heart disease prediction using clinical data from Kaggle. The study employs Generalized Linear Models (GLMs) with logit, probit, and complementary log-log links to identify key risk factors and build predictive models for heart disease probability.

## 🎯 Objectives
1. Identify which clinical features significantly impact heart disease probability
2. Assess how and to what extent these factors influence disease probability
3. Build statistical models to predict individual heart disease risk

## 📁 Dataset
**Source**: [Kaggle Heart Failure Prediction Dataset](https://www.kaggle.com/fedesoriano/heart-failure-prediction)

**Size**: 918 observations (balanced: 508 heart disease, 410 normal)

**Features**: 11 clinical predictors including Age, Sex, ChestPainType, RestingBP, Cholesterol, FastingBS, RestingECG, MaxHR, ExerciseAngina, Oldpeak, ST_Slope

## 🔬 Methodology
- **Exploratory Data Analysis**: Numerical summaries, distribution visualizations, correlation analysis
- **Statistical Modeling**: Sequential log-likelihood ratio tests for variable selection
- **Three Link Functions**: Logit, Probit, Complementary Log-log
- **Model Diagnostics**: Pearson chi-squared, Hosmer-Lemeshow, AIC/BIC comparison

## 📈 Key Findings
### Significant Predictors:
- **Strong Positive Association**: Male sex (OR = 4.28), Exercise-induced angina (OR = 2.69), Flat ST slope (OR = 4.23)
- **Strong Negative Association**: Cholesterol levels, Atypical chest pain types

### Model Performance:
- **Probit Model**: Lowest deviance (596.27) and AIC (620.27)
- **Logit Model**: Lowest BIC (674.65), most interpretable
- All models passed goodness-of-fit tests (p > 0.05)

## 🛠️ Technical Implementation

### Dependencies
```r
# Required R packages
install.packages(c("ggplot2", "corrplot", "ggpubr", "knitr", "dplyr", "kableExtra"))
