# Data-Science-Jobs-Salary-Prediction
- The aim is to predict Data Scientist salary based on job descriptions
- Data collected by web scrapping of job descriptions from glassdoor.com using python and selenium
- Cleaned the data to extract salary, job_roles, skills required (python, sql, statistics etc.) and other features
- Explored the data to understand relationship of various features with the target (salary)
- Applied mean-encoding to categorical features
- Optimized Linear, Lasso, and Random Forest Regressors using GridsearchCV to obtain the best model
## PART A. DATA COLLECTION
- Data collected by web scrapping of job descriptions from glassdoor.com using python and selenium
- This article was referenced to obtain data: https://towardsdatascience.com/selenium-tutorial-scraping-glassdoor-com-in-10-minutes-3d0915c6d905
## PART B. DATA CLEANING
Following things are done:
- Removed all such instances where the target label (salary) was missing from the data
- Extracted salary data in numeric format out of salary_estimate
- Converted 'per hour' and 'employer provided salary' into annual salary
- Added columns indicating age of company, job location (state) and headquarter job or not
- Extracted different skills from job description and indicated them new columns:
  - Python,
  - SQL,
  - Machine Learning, 
  - Statistics, 
  - Excel, 
  - AWS/Azure, 
  - Spark/Hadoop, 
  - Tableau/PowerBI, 
  - TensorFlow/Pytorch
## PART C. EXPLORATORY DATA ANALYSIS
- Calculated percentage of jobs per category within each variable and also the average of target value (ie. avg_sal) per category
- Plotted these values for different variables to understand relationship of various features with the target
## PART D. FEATURE ENGINEERING
- Applied mean-encoding to categorical features to obtain monotonic relationship between features and target
## PART E. MODEL BUILDING
Implemented three different models:
- Multiple Linear Regression
- Lasso Regression
- Random Forest
### Model performance:
- Random Forest : MAE = 10.3344
- Lasso Regression: MAE = 15.8358
- Linear Regression: MAE = 16.1901
