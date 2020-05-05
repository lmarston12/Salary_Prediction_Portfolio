# Salary_Prediction_Portfolio
Salary Prediction Project (python)
## Project Summary
This project will predict salaries based on job descriptions and features. There a many factors that go into determining salary such as: Education of a person, number of years of experience, seniority in the company, type of industry, distance from a major city, etc. The Salary Prediction Project will help candidates estimate salaries in a new job and could give companies a better understanding of what they should pay a new hire.

In this project, I develop 3 models (Linear Regression, Random Forest Regression, and Gradient Boosting Regression) and identify the best model to use by comparing the Mean Squared Errors (MSE).

## 1. Intro
The training data is split into two CSV files, one for the features given and one for the target variable. The test data contains the Job IDs and the features we need to use to predict the salaries. All of the data sets used contained ~1000000 data entries. The following are the features used and the associated descriptions:

JobId: The ID of job. It is unique for every employee.
companyid: The ID of company.
JobType: The designation in the company.
degree: Highest degree of a Employee.
major: The field or subject on which, employee had completed his/her degree from university.
industry: The field of company like Health, Finance, Oil etc.
YearsofExperience: Years of experiene of an employee in the job.
milesFromMetropolis: The distance, in miles, the job is from a major city.
salary: This is the target variable. It is the yearly salary of the employee.

## Data Preprocessing 
One thing I did  to further process and clean the data was to check for duplicates and invalid data. I found no duplicates in the datasets, but I did notice that there were 5 data entries with a salary of 0. After further analysis, these entries were removed becuase there was no indication that these jobs would be 'volunteer' work and they did not make sense to keep in the dataset.

## Exploratory Data Analysis
Before diving into the machine learning algorithms, I performed exploratory data analysis (EDA) to identify significant features that affect the salary. I found that some of the features have trends with salary and I visualized them below:


INSERT VISUALIZATIONS HERE


I also wanted to look for outliers in the data (using IQR Rule). The salaries seem to be normally distributed. After analyzing salaries above the upper IQR value, it appeared that all of these entries seemed legitimate because most of the roles were excutive level with ~20+ years of experience in high paying industries so these entries were not removed.

INSERT BOX PLOT VISUAL HERE
