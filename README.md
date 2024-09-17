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
The approach for this project involved a structured methodology. Initially, I performed a comprehensive exploration of the dataset to understand the significance of each variable. This was followed by an extensive exploratory data analysis (EDA) to uncover key insights, while also cleaning the data to address any missing or duplicated entries. Subsequently, I developed machine learning models, including logistic regression, decision tree, and random forest, leveraging the PACE framework to ensure robust performance. I also employed feature engineering to ensure that only the most relevent features were used to train the models. 
The results were thoroughly analyzed, and based on the findings from both the EDA and the models, I provided actionable recommendations to the company.

## Model Results

### Logistic Regression
The logistic regression model achieved the following results on the test set:

- **Precision**: 80%
- **Recall**: 83%
- **F1-Score**: 81% (weighted average)
- **Accuracy**: 83%

![Insert Logistic Regression Performance Graph here](https://github.com/DSM2499/HR_Analytics/blob/main/Photos/CM_Log_reg.png?raw=true)

---

### Decision Tree
After feature engineering, the decision tree model yielded the following results on the test set:

- **AUC**: 95.8%
- **Precision**: 82.0%
- **Recall**: 89.3%
- **F1-Score**: 85.2%
- **Accuracy**: 94.85%

![Insert Decision Tree Performance Graph here](https://github.com/DSM2499/HR_Analytics/blob/main/Photos/DT_Plot.png?raw=true)
![](https://github.com/DSM2499/HR_Analytics/blob/main/Photos/DT_feature_Imp.png?raw=true)

---

### Random Forest
The random forest model modestly outperformed the decision tree model.

- **AUC**: 96.60%
- **Precision**: 86.56%
- **Recall**: 89.62%
- **F1-Score**: 88.10%
- **Accuracy**: 95.94%

![Insert Random Forest Performance Graph here](https://github.com/DSM2499/HR_Analytics/blob/main/Photos/RF_CM.png?raw=true)
![](https://github.com/DSM2499/HR_Analytics/blob/main/Photos/RF_Feature_Imp.png?raw=true)

## Conclusion, Recommendations and Next Steps:
Based on the analysis, it is evident that employee workload and satisfaction levels are key factors influencing employee turnover at Sailfort Motors. The data revealed that employees who worked either significantly fewer or significantly more hours than their peers were more likely to leave the company. Specifically, employees who worked on six or more projects, often logging between 255 to 310 hours per month, experienced high rates of turnover. In contrast, employees who worked on three to four projects exhibited a much lower turnover rate, suggesting that this may be the optimal workload for retention.

Additionally, employees who left the company tended to fall into distinct groups: those who worked long hours with low satisfaction and those who had relatively normal working hours but still reported low satisfaction. These insights highlight the importance of balancing workload and ensuring that employees are satisfied with their roles.

Further analysis showed that employees at the four-year mark are more likely to leave due to low satisfaction levels, which may indicate dissatisfaction with policies or work conditions during this tenure period. Employees with longer tenures, however, generally had higher satisfaction levels, indicating that these employees may hold higher-ranking positions and be less inclined to leave.

Finally, the machine learning models confirmed that overworking employees is a significant factor contributing to turnover. This reinforces the need for stakeholders to address workload management and employee recognition.

### Recommendations:
- **Cap the Number of Projects**: Limit the number of projects employees can be assigned to, with three to four projects being the optimal range to prevent burnout.
- **Investigate Employee Satisfaction at the Four-Year Mark**: Conduct an internal review to understand why employees at this stage report lower satisfaction and address potential policy or workload issues.
- **Balance Long Working Hours with Rewards**: Either reduce the expectation for long working hours or introduce rewards and incentives for employees who consistently put in extra effort to prevent dissatisfaction and burnout.
- **Revise Evaluation Metrics**: Ensure that high performance evaluations are not solely based on the number of hours worked. Implement a more balanced system that rewards both effort and efficiency, ensuring employees who contribute effectively without overworking are recognized.

### Next Steps
- It may be justified to still have some concern about data leakage. It could be prudent to consider how predictions change when last_evaluation is removed from the data. It's possible that evaluations aren't performed very frequently, in which case it would be useful to be able to predict employee retention without this feature. It's also possible that the evaluation score determines whether an employee leaves or stays, in which case it could be useful to pivot and try to predict performance score. The same could be said for satisfaction score.
- For another project, you could try building a K-means model on this data and analyzing the clusters. This may yield valuable insight.
