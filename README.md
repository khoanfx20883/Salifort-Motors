# Salifort-Motors
## HR Analytics Job Prediction
### Scenario:  
Salifort makes a big investment in recruiting, training, and upskilling its employees. If Salifort could predict whether an employee will leave the company, and discover the reasons behind their departure, they could better understand the problem and develop a solution. 

### Dataset:  
https://www.kaggle.com/datasets/mfaisalqureshi/hr-analytics-and-job-prediction?select=HR_comma_sep.csv

### Objective: 
I choose an approach to deploy both logistic regression and XGBoost for building the most effective model to predict employee departure.

### Method: 
XGBoost often handles class imbalance and multicollinearity better than logistic regression due to its ensemble nature and regularization techniques. The logistic regression model provides a better understanding of the linear relationship between the feature variables and the predicted outcome, while XGBoost provides insight into the importance of each feature in improving the model. Combining these two methods allows you to both make better predictions and clearly explain the relationship between the variables and the target outcome.

### Results: 
The recall rate for class '1' is 95%, meaning that the model correctly predicted 95% of the employees who would actually leave. This is important because you want to make sure that the model is able to identify most of the cases that are likely to leave. There were only 9 cases where the model incorrectly predicted employees who would leave (False Positives), which shows that the model is very unlikely to generate false alarms. The regression coefficient shows that as an employee's years of service at the company increases, their likelihood of leaving also increases. As the number of projects an employee is involved in and their recent performance review scores increase, the likelihood of them quitting decreases.

### Challenges: 
There is a disproportionate ratio of instances between different classes, leading to biased models that misclassify the minority class and result in poor classification performance. Upsample the minority class from 17% to 30% has the potential to significantly improve the Recall and Precision of the minority class, but needs to be carefully monitored to avoid overfitting. Upsample to 20% can be a safer solution to avoid overfitting, especially if you care about the generalization ability of the model on new data.

### Scope of use: 
Helping the company increase retention and job satisfaction for current employees, and save money and time training new employees. 

### Usage instructions: 
Run the source code in the Salifort_Motors.ipynb file in Jupyter Notebook with Python version 3.11.5 to load data from the HR_comma_sep.csv file. The results are presented in the Executive Summary.docx file.
