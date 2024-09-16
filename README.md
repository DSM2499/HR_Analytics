# Employee Retention Project

## Overview
This project focuses on addressing a critical challenge for Sailfort Motors, a fictional company, by developing a method to analyze employee data. The goal is to identify key factors influencing employee turnover and implement strategies to enhance employee retention.

## Dataset
The dataset used contains 15,000 rows and 10 columns for the variables listed below. 

**Note:** Dataset was found on [Kaggle](https://www.kaggle.com/datasets/mfaisalqureshi/hr-analytics-and-job-prediction?select=HR_comma_sep.csv).

Variable  |Description |
-----|-----|
satisfaction_level|Employee-reported job satisfaction level [0&ndash;1]|
last_evaluation|Score of employee's last performance review [0&ndash;1]|
number_project|Number of projects employee contributes to|
average_monthly_hours|Average number of hours employee worked per month|
time_spend_company|How long the employee has been with the company (years)
Work_accident|Whether or not the employee experienced an accident while at work
left|Whether or not the employee left the company
promotion_last_5years|Whether or not the employee was promoted in the last 5 years
Department|The employee's department
salary|The employee's salary (U.S. dollars)

## Approach
The approach for this project involved a structured methodology. Initially, I performed a comprehensive exploration of the dataset to understand the significance of each variable. This was followed by an extensive exploratory data analysis (EDA) to uncover key insights, while also cleaning the data to address any missing or duplicated entries. Subsequently, I developed machine learning models, including logistic regression, decision tree, and random forest, leveraging the PACE framework to ensure robust performance. The results were thoroughly analyzed, and based on the findings from both the EDA and the models, I provided actionable recommendations to the company.

## Model Results

### Logistic Regression
The logistic regression model achieved the following results on the test set:

- **Precision**: 80%
- **Recall**: 83%
- **F1-Score**: 81% (weighted average)
- **Accuracy**: 83%

![Insert Logistic Regression Performance Graph here](path_to_image)

---

### Decision Tree
After feature engineering, the decision tree model yielded the following results on the test set:

- **AUC**: 95.8%
- **Precision**: 82.0%
- **Recall**: 89.3%
- **F1-Score**: 85.2%
- **Accuracy**: 94.85%

![Insert Decision Tree Performance Graph here](path_to_image)

---

### Random Forest
The random forest model modestly outperformed the decision tree model.

- **AUC**: 96.60%
- **Precision**: 86.56%
- **Recall**: 89.62%
- **F1-Score**: 88.10%
- **Accuracy**: 95.94%

![Insert Random Forest Performance Graph here](path_to_image)
