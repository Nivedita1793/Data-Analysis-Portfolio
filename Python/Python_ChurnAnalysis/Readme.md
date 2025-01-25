# Customer Churn Analytics and Predictive Modeling

## Overview
This project focuses on analyzing customer churn in an e-commerce platform. The analysis includes data cleaning, exploratory data analysis (EDA), predictive modeling, and insights to improve customer retention. The following steps outline the methodology and findings.

---

## Steps Involved

### 1. **Data Import and Overview**
- Imported libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `plotly`.
- Loaded the dataset into a pandas DataFrame.
- Explored data using `.head()`, `.info()`, and `.describe()`.
- Identified missing values in key columns like:
  - `Tenure`
  - `WarehouseToHome`
  - `HourSpendOnApp`
  - `OrderAmountHikeFromlastYear`
  - `CouponUsed`
  - `OrderCount`
  - `DaySinceLastOrder`.

### 2. **Data Cleaning**

#### Data Standardization:
- Replaced values in categorical columns for consistency:
  - `PreferredPaymentMode`: 'Credit Card' to 'CC', 'Cash on Delivery' to 'COD'.
  - `PreferredLoginDevice`: 'Phone' to 'Mobile Phone'.
  - `PreferedOrderCat`: 'Mobile' to 'Mobile Phone'.

#### Handling Missing Values:
- Imputed missing values using:
  - Median for skewed distributions.
  - Mode for categorical-like variables.

#### Outlier Detection:
- Identified outliers in numeric columns using box plots.
- Calculated IQR and set limits for potential outliers in:
  - `WarehouseToHome`
  - `DaySinceLastOrder`
  - `CouponUsed`
  - `OrderCount`.

### 3. **Exploratory Data Analysis (EDA)**

#### Churn Distribution:
- Visualized churned vs. non-churned customers using a pie chart.

#### Churn vs. Key Features:
- Analyzed relationships between churn and features:
  - Boxplots: `Tenure`, `OrderCount`.
  - Bar plots: `PreferredPaymentMode`, `CityTier`, `SatisfactionScore`, `Complain`.

#### Correlation Analysis:
- Visualized correlation matrix to identify relationships between features.

### 4. **Data Preprocessing for Model Building**
- Applied one-hot encoding to categorical variables.

### 5. **Baseline Model: Decision Tree**

#### Model Training:
- Trained a Decision Tree classifier.
- Performed hyperparameter tuning using GridSearchCV.

#### Model Evaluation:
- Evaluated performance using accuracy score and classification report.
- Visualized decision tree structure.

#### Feature Importance:
- Identified features like `Tenure`, `Complain`, `Cashback Amount`, and `Order Count` as key churn predictors.

#### Predictive Analysis:
- Segmented customers into high-risk and low-risk groups based on predictions.
- Stored results in a CSV file and visualized churn predictions using a pie chart.

### 6. **Baseline Model: Logistic Regression**

#### Model Training:
- Trained a Logistic Regression model on preprocessed data.

#### Model Evaluation:
- Evaluated performance using accuracy score, classification report, and confusion matrix.

#### Predictive Analysis:
- Performed similar analysis as with the Decision Tree model.
- Stored predictions and visualized churn distribution.

### 7. **Summary**
- Key features influencing churn: `Tenure`, `Complain`, `Cashback Amount`, `Order Count`, `Days Since Last Order`.
- Retention recommendations based on findings:
  - Improve customer satisfaction.
  - Address complaints promptly.
  - Offer personalized rewards for loyalty.

- Compared Decision Tree and Logistic Regression models for performance.

---

## Key Tools and Techniques
- **Tools:** Python (`pandas`, `matplotlib`, `seaborn`, `scikit-learn`, `plotly`).
- **Techniques:** Data cleaning, EDA, predictive modeling, feature importance analysis.

---

## Results
- Churn prediction models provide actionable insights into customer retention.
- Highlighted customer segments at high risk of churn.

---

## Repository
Access the code and resources in this repository.
