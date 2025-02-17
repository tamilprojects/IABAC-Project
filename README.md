## Business Case:


INX Future Inc Employee Performance - Project

INX Future Inc , (referred as INX ) , is one of the leading data analytics and automation solutions provider with over 15 years of global business presence. INX is consistently rated as top 20 best employers past 5 years. INX human resource policies are considered as employee friendly and widely perceived as best practices in the industry.

Recent years, the employee performance indexes are not healthy and this is becoming a growing concerns among the top management. There has been increased escalations on service delivery and client satisfaction levels came down by 8 percentage points.

CEO, Mr. Brain, knows the issues but concerned to take any actions in penalizing non-performing employees as this would affect the employee morale of all the employees in general and may further reduce the performance. Also, the market perception best employer and thereby attracting best talents to join the company.

Mr. Brain decided to initiate a data science project , which analyses the current employee data and find the core underlying causes of this performance issues. Mr. Brain, being a data scientist himself, expects the findings of this project will help him to take right course of actions. He also expects a clear indicators of non performing employees, so that any penalization of non-performing employee, if required, may not significantly affect other employee morals.


# Employee Performance Analysis

## Project Summary

### Business Case & Goal of the Project

The objective is to predict the performance rating of employees using the given dataset features.

This project involves analyzing employee performance based on various factors. The primary goal is:

1. To develop a trained model capable of predicting employee performance.
2. To provide actionable recommendations for improving employee performance based on insights.

### Dataset Overview

- **Rows:** 1200
- **Columns:** 28 (19 quantitative and 8 qualitative features)
- **Target Variable:** Performance Rating (Ordinal)

### Key Points:

- **Machine Learning Models Used:**
  - Support Vector Classifier
  - Random Forest Classifier
  - Artificial Neural Network (Multilayer Perceptron)
  - Best Model: Artificial Neural Network with 95.80% accuracy
- **Preprocessing Techniques:**
  - Manual and frequency encoding for categorical data
  - Handling outliers using IQR
  - Data scaling with Standard Scaler
  - Dimensionality reduction with PCA
- **Important Factors Identified:**
  - Employee Environment Satisfaction
  - Employee Salary Hike Percentage
  - Experience Years in Current Role

---

## Analysis Process

### 1. Data Analysis

#### Feature Classification:

- **Categorical Features:**
  - EmpNumber, Gender, EducationBackground, MaritalStatus, EmpDepartment, EmpJobRole, BusinessTravelFrequency, OverTime, Attrition
- **Numerical Features:**
  - Age, DistanceFromHome, EmpHourlyRate, NumCompaniesWorked, EmpLastSalaryHikePercent, TotalWorkExperienceInYears, TrainingTimesLastYear, ExperienceYearsAtThisCompany, ExperienceYearsInCurrentRole, YearsSinceLastPromotion, YearsWithCurrManager
- **Ordinal Features:**
  - EmpEducationLevel, EmpEnvironmentSatisfaction, EmpJobInvolvement, EmpJobLevel, EmpJobSatisfaction, EmpRelationshipSatisfaction, EmpWorkLifeBalance, PerformanceRating

### 2. Univariate, Bivariate & Multivariate Analysis

- **Tools:** Matplotlib, Seaborn
- **Plots:** Histplot, Lineplot, Countplot, Barplot
- **Insights:**
  - Features like **EmpEnvironmentSatisfaction**, **EmpLastSalaryHikePercent**, and **EmpWorkLifeBalance** positively correlate with performance rating.

---

## Exploratory Data Analysis (EDA)

### Key Observations:

- **Distribution of Features:**
  - Most employees are aged between 30 to 40.
  - Majority worked in up to two companies before joining.
  - Employees typically get a salary hike of 11-15%.
  - Most employees have 5 years of experience at the company.
- **Skewness & Kurtosis:**
  - YearsSinceLastPromotion is skewed with a skewness of 1.97 and kurtosis of 3.52.

---

## Data Preprocessing

1. **Missing Values:** None found.
2. **Categorical Data Conversion:**
   - Manual and frequency encoding used.
3. **Outlier Handling:**
   - Handled using the IQR method.
4. **Feature Transformation:**
   - Square Root Transformation applied to skewed features.
   - Q-Q plot used to confirm normalization.
5. **Scaling:**
   - Standard Scaling applied.

---

## Feature Selection

1. Dropped unique and constant features (e.g., EmpNumber, YearsSinceLastPromotion).
2. Checked correlations using a heatmap.
3. Applied PCA:
   - Reduced 27 features to 25 with minimal variance loss.
4. No duplicate records were found.
5. Saved preprocessed data for model training.

---

## Machine Learning Model Creation & Evaluation

### Steps:

1. **Balancing Data:** Applied SMOTE to address class imbalance.
2. **Data Split:** 80% training, 20% testing.
3. **Models Used:**
   - Support Vector Classifier:
     - Training Accuracy: 97.13%
     - Testing Accuracy: 94.85%
     - After Hyperparameter Tuning: 91.28%
   - Random Forest:
     - Training Accuracy: 100%
     - Testing Accuracy: 96.19%
     - Overfitting observed after tuning.
   - Artificial Neural Network (MLP):
     - Training Accuracy: 99.76%
     - Testing Accuracy: 95.61%

### Selected Model:

- Artificial Neural Network (MLP) due to consistent performance.

---

## Department-Wise Performance

### Key Insights:

1. **Sales:**
   - Level 3 performers dominate.
   - Male employees slightly outperform females.
2. **Human Resources:**
   - Majority at Level 3.
   - Older employees show lower performance.
   - Female employees perform better overall.
3. **Development:**
   - Consistent Level 3 performance across ages and genders.
4. **Data Science:**
   - Highest performance overall.
   - Male employees slightly outperform.
5. **Research & Development:**
   - Performance is independent of age.
   - Female employees perform well.
6. **Finance:**
   - Performance declines with age.
   - Male employees perform better.

---

## Top 3 Factors Affecting Performance

1. **Employee Environment Satisfaction:**
   - Levels 3 and 4 correspond to higher performance.
2. **Employee Salary Hike Percentage:**
   - Employees with hikes of 11-19% perform at Levels 2 and 3.
   - Hikes of 20-22% lead to Level 4 performance.
3. **Employee Work-Life Balance:**
   - Level 3 shows the highest performance ratings.

---

## Recommendations to Improve Performance

1. **Enhance Employee Environment Satisfaction:**
   - Focus on improving workplace conditions.
2. **Salary Hikes:**
   - Implement frequent and fair salary hikes.
3. **Promotions:**
   - Conduct evaluations and promotions every 6 months.
4. **Work-Life Balance:**
   - Provide flexibility to employees for better balance.
5. **Department-Specific Recommendations:**
   - **HR:** Focus on recruiting more female employees.
   - **Sales & Development:** Continue nurturing as these departments show high performance.
   - Address feedback from employees with low and medium job satisfaction, as they often outperform.

---

## Tools & Libraries Used

### Tools:

- Jupyter Notebook

### Libraries:

- Pandas
- NumPy
- Matplotlib
- Seaborn
- PyLab
- SciPy
- Scikit-learn
- Pickle
