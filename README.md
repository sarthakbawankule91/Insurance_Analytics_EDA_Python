# 🛡️ Insurance Analytics – Data Analysis & Machine Learning

## 📌 Project Overview

This project focuses on analyzing an insurance dataset to identify customer, policy, claim, fraud, and risk patterns using **Python, Exploratory Data Analysis (EDA), Machine Learning, and Customer Segmentation**.

The project uses insurance customer and policy information to generate insights that can support:

* Insurance premium prediction
* Fraud detection
* Customer risk segmentation
* Claim analysis
* Policy analysis
* Data-driven business recommendations

The analysis was performed using **Python and Jupyter Notebook**.

---

## 🎯 Problem Statement

Insurance companies handle large amounts of customer, policy, vehicle, premium, and claim data.

The objective of this project is to analyze insurance data and answer important business questions such as:

* What factors influence insurance premiums?
* Which claims may be fraudulent?
* How are customers distributed across different risk segments?
* What customer and policy characteristics are associated with claims?
* Which features contribute most to premium prediction?
* How can insurance companies improve pricing, fraud detection, and customer retention?

---

## 📊 Dataset Information

The original dataset contains **15,000 records and 39 columns**.

After data cleaning and preprocessing, the cleaned dataset contains **14,884 records and 39 columns**.

### Dataset Categories

The dataset contains information related to:

* Customer demographics
* Financial information
* Vehicle details
* Insurance policies
* Claims
* Fraud indicators
* Premiums
* Risk information

---

## 📋 Dataset Features

| Feature              | Description                    |
| -------------------- | ------------------------------ |
| `Customer_ID`        | Unique customer identifier     |
| `Policy_ID`          | Unique policy identifier       |
| `Claim_ID`           | Unique claim identifier        |
| `Age`                | Customer age                   |
| `Gender`             | Customer gender                |
| `Marital_Status`     | Marital status                 |
| `Education`          | Education level                |
| `Occupation`         | Customer occupation            |
| `Region`             | Customer region                |
| `Annual_Income`      | Annual customer income         |
| `Credit_Score`       | Customer credit score          |
| `Vehicle_Make`       | Vehicle manufacturer           |
| `Vehicle_Model`      | Vehicle model                  |
| `Vehicle_Type`       | Type of vehicle                |
| `Vehicle_Age`        | Age of vehicle                 |
| `Vehicle_Value`      | Vehicle value                  |
| `Engine_Size`        | Engine size                    |
| `Mileage`            | Vehicle mileage                |
| `Policy_Type`        | Insurance policy type          |
| `Coverage_Amount`    | Insurance coverage amount      |
| `Deductible`         | Policy deductible              |
| `Policy_Start_Date`  | Policy start date              |
| `Policy_End_Date`    | Policy end date                |
| `Previous_Policies`  | Number of previous policies    |
| `Number_of_Claims`   | Number of claims               |
| `Claim_Amount`       | Claim amount                   |
| `Accident_Severity`  | Accident severity              |
| `Police_Report`      | Police report status           |
| `Witness_Present`    | Witness availability           |
| `Days_to_Report`     | Days taken to report claim     |
| `Hospital_Bills`     | Hospital expenses              |
| `Repair_Cost`        | Vehicle repair cost            |
| `Premium`            | Insurance premium              |
| `Fraudulent_Claim`   | Fraud status                   |
| `Claim_Status`       | Claim status                   |
| `BMI`                | Customer BMI                   |
| `Driving_Experience` | Driving experience             |
| `Risk_Score`         | Customer risk score            |
| `Customer_Tenure`    | Customer relationship duration |

---

## 🛠️ Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Seaborn**
* **Scikit-learn**
* **Jupyter Notebook**
* **Excel**

### Machine Learning Algorithms

#### Regression

* Linear Regression
* Decision Tree Regressor
* Random Forest Regressor
* Gradient Boosting Regressor
* Extra Trees Regressor
* AdaBoost Regressor

#### Classification

* Logistic Regression
* Decision Tree Classifier
* Random Forest Classifier
* Gradient Boosting Classifier
* Extra Trees Classifier
* AdaBoost Classifier

#### Clustering

* K-Means Clustering

---

# 🔍 Project Workflow

```text
Raw Insurance Data
        ↓
Data Quality Assessment
        ↓
Data Cleaning & Preprocessing
        ↓
Exploratory Data Analysis
        ↓
Premium Prediction
        ↓
Fraud Detection
        ↓
Customer Segmentation
        ↓
Business Recommendations
```

---

# 🧹 1. Data Cleaning & Preprocessing

The raw insurance dataset was analyzed and cleaned before performing further analysis.

The preprocessing workflow included:

* Checking dataset structure
* Identifying missing values
* Checking duplicate records
* Standardizing categorical values
* Handling inconsistent data
* Converting date columns
* Creating policy-duration features
* Handling missing numerical values
* Preparing data for machine learning

The cleaned dataset contains:

```text
14,884 records
39 columns
```

---

# 📊 2. Exploratory Data Analysis

EDA was performed to understand customer, policy, vehicle, premium, and claim characteristics.

### Customer Analysis

The following characteristics were analyzed:

* Age distribution
* Gender
* Marital status
* Occupation
* Education
* Region
* Annual income

### Policy Analysis

Policy-related analysis included:

* Policy type distribution
* Premium distribution
* Policy duration
* Coverage amount
* Deductible

### Vehicle Analysis

Vehicle characteristics analyzed:

* Vehicle type
* Vehicle make
* Vehicle age
* Vehicle value
* Engine size
* Mileage

### Claim Analysis

Claim-related analysis included:

* Claim status
* Claim amount
* Accident severity
* Police report
* Witness presence
* Days to report
* Hospital bills
* Repair cost

---

# 📈 Important EDA Findings

### Fraud Distribution

The dataset shows:

| Fraud Status      | Percentage |
| ----------------- | ---------: |
| Genuine Claims    |     90.51% |
| Fraudulent Claims |      9.49% |

This indicates that fraudulent claims represent a smaller portion of the overall claims but still require monitoring.

---

### Premium by Policy Type

Average premium by policy type:

| Policy Type | Average Premium |
| ----------- | --------------: |
| Silver      |       35,329.47 |
| Gold        |       35,260.33 |
| Basic       |       35,252.48 |
| Platinum    |       35,162.52 |

---

### Average Claim Amount by Vehicle Type

| Vehicle Type | Average Claim Amount |
| ------------ | -------------------: |
| SUV          |            93,139.08 |
| Sedan        |            92,493.14 |
| Hatchback    |            92,006.62 |

---

### Policy Duration

The calculated policy duration has:

* Minimum: **365 days**
* Average: **1,073.66 days**
* Median: **1,095 days**
* Maximum: **1,825 days**

---

# 🤖 3. Premium Prediction

## Objective

Develop a regression model to predict the **annual insurance premium** based on customer, policy, vehicle, financial, and claim-related characteristics.

### Target Variable

```text
Premium
```

### Features Used

Examples include:

* Age
* Gender
* Vehicle Age
* Annual Income
* Risk Score
* Claim History
* Policy Type
* Vehicle Type
* Claim Amount
* Vehicle Value
* Mileage
* Customer Tenure

---

## 🔄 Machine Learning Preprocessing

The following steps were performed:

### 1. Date Feature Engineering

Policy dates and claim dates were converted into useful components:

* Year
* Month
* Day

Policy duration was also calculated.

### 2. Categorical Encoding

Categorical variables were converted into numerical values using `LabelEncoder`.

### 3. Missing Value Imputation

Missing numerical values were handled using median imputation.

### 4. Train-Test Split

```text
80% → Training Data
20% → Testing Data
```

### 5. Feature Scaling

`StandardScaler` was used to standardize the features.

---

# 📊 Regression Model Performance

The models were evaluated using:

* MAE
* RMSE
* R² Score

| Model             |      MAE |     RMSE | R² Score |
| ----------------- | -------: | -------: | -------: |
| Gradient Boosting | 2,043.22 | 2,368.89 |   0.9448 |
| Random Forest     | 2,081.40 | 2,443.71 |   0.9412 |
| Extra Trees       | 2,221.99 | 2,697.33 |   0.9284 |
| Linear Regression | 2,338.30 | 3,196.22 |   0.8995 |
| Decision Tree     | 2,802.98 | 3,446.32 |   0.8831 |
| AdaBoost          | 2,845.47 | 3,490.89 |   0.8801 |

The notebook selected **Gradient Boosting Regressor** based on the model comparison.

### Model Performance

```text
R² Score : 0.9448
MAE      : 2,043.22
RMSE     : 2,368.89
```

---

# 🔎 Premium Prediction – Feature Importance

The Gradient Boosting model's feature importance analysis identified the following major contributors:

| Feature          | Importance |
| ---------------- | ---------: |
| Number of Claims |     0.5047 |
| Annual Income    |     0.4606 |
| Age              |     0.0337 |
| Repair Cost      |     0.0001 |
| Claim ID         |     0.0001 |

The model therefore placed substantial importance on **Number of Claims and Annual Income** for premium prediction in this dataset.

---

# 🚨 4. Fraud Detection

## Objective

Build a machine learning classification model to identify whether an insurance claim is:

```text
0 → Genuine Claim
1 → Fraudulent Claim
```

This is a **Binary Classification Problem**.

### Target Variable

```text
Fraudulent_Claim
```

### Features

The model uses customer, policy, vehicle, and claim-related variables to classify claims.

---

## Fraud Analysis

The project analyzes fraud using:

* Policy type
* Claim amount
* Premium
* Customer age
* Vehicle information
* Claim history
* Other customer and policy characteristics

A policy-type fraud analysis was also performed.

---

# 👥 5. Customer Segmentation

## Objective

Customers were grouped into different risk categories using **K-Means Clustering**.

The goal is to identify customer groups based on:

* Age
* Annual Income
* Credit Score
* Vehicle Age
* Vehicle Value
* Number of Claims
* Claim Amount
* Driving Experience
* Mileage
* BMI
* Risk Score
* Customer Tenure

---

## 🔬 Clustering Process

### Step 1 – Feature Selection

Relevant customer risk features were selected.

### Step 2 – Feature Scaling

`StandardScaler` was used because K-Means relies on distance calculations.

### Step 3 – Elbow Method

WCSS was calculated for different values of `K`.

### Step 4 – K-Means

The project uses:

```python
KMeans(
    n_clusters=3,
    random_state=42,
    n_init=10
)
```

Three customer segments were created.

---

## 🏷️ Customer Risk Segments

The clusters were interpreted as:

```text
Cluster 0 → Low Risk
Cluster 1 → Medium Risk
Cluster 2 → High Risk
```

The segmentation considers customer demographic, financial, vehicle, and claims-related characteristics.

---

# 💼 6. Business Recommendations

## 🚨 Improve Fraud Detection

### Observation

Fraudulent claims represent **9.49%** of the claims in the dataset.

### Recommendations

* Use machine learning to flag potentially suspicious claims.
* Manually review high-risk and high-value claims.
* Verify supporting documents before approving high-value claims.
* Monitor repeated suspicious claims.
* Investigate unusually high claim amounts.
* Continuously update fraud detection models with new claim data.

### Business Impact

* Reduce financial losses.
* Improve fraud monitoring.
* Speed up processing for genuine claims.
* Improve operational efficiency.

---

# 💰 Optimize Premium Pricing

### Observation

Customer and claim characteristics can be used to support premium prediction.

The Gradient Boosting model achieved an R² score of approximately **0.945** on the test data.

### Recommendations

* Use risk-based pricing.
* Consider claim history when pricing policies.
* Reward lower-risk customers.
* Review premiums using updated customer risk information.
* Explore usage-based insurance and telematics.

### Business Impact

* Improve pricing accuracy.
* Reduce losses from underpriced high-risk policies.
* Support competitive insurance pricing.

---

# 👥 Improve Customer Segmentation

Customer segmentation can support differentiated strategies for different risk groups.

### Low Risk

Potential strategies:

* Loyalty rewards
* Renewal benefits
* Personalized offers
* Premium plans

### Medium Risk

Potential strategies:

* Standard pricing
* Personalized discounts
* Renewal reminders
* Safe-driving incentives

### High Risk

Potential strategies:

* Risk-based pricing
* Higher deductibles where appropriate
* Telematics-based monitoring
* Defensive-driving programs

---

# 📊 7. Business Dashboard

The project can also be presented through an interactive **Power BI dashboard** covering:

### KPI Section

* Total Customers
* Total Policies
* Total Claims
* Total Premium
* Average Premium
* Total Claim Amount
* Fraud Rate
* Average Risk Score

### Customer Analysis

* Customer distribution
* Age groups
* Region
* Occupation
* Customer risk segments

### Policy Analysis

* Policy type
* Premium distribution
* Coverage amount
* Policy duration

### Claims Analysis

* Claim status
* Claim amount
* Accident severity
* Claim trends
* Fraudulent vs genuine claims

### Risk Analysis

* Low Risk
* Medium Risk
* High Risk

---

# 📌 Key Project Outcomes

This project demonstrates how insurance data can be used to:

* Understand customer behavior
* Analyze insurance policies
* Identify claim patterns
* Predict insurance premiums
* Detect potentially fraudulent claims
* Segment customers according to risk
* Develop data-driven business recommendations
* Support insurance pricing and risk management

---

# 🧠 Skills Demonstrated

### Data Analytics

* Data Cleaning
* Data Preprocessing
* Exploratory Data Analysis
* Statistical Analysis
* Data Visualization
* Feature Engineering

### Python

* Pandas
* NumPy
* Matplotlib
* Seaborn

### Machine Learning

* Regression
* Classification
* Clustering
* Feature Encoding
* Feature Scaling
* Model Evaluation
* Feature Importance

### Business Analytics

* Risk Analysis
* Premium Analysis
* Fraud Analysis
* Customer Segmentation
* Business Recommendations
* KPI Development

---

# 📂 Project Structure

```text
Insurance-Analytics/
│
├── Insurance_Analytics_Data.xlsx
├── Insurance_Analytics_Cleaned_Data.xlsx
├── Insurance_Analytics_proj.ipynb
├── Premium_Prediction_Model.pkl
└── README.md
```

---

# 🚀 How to Run the Project

### 1. Clone the Repository

```bash
git clone <your-github-repository-url>
```

### 2. Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn scikit-learn openpyxl joblib
```

### 3. Open Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
Insurance_Analytics_proj.ipynb
```

### 4. Keep the Dataset in the Project Folder

Make sure the Excel dataset is available in the same directory as the notebook.

---

# 👨‍💻 Author

**Sarthak Bawankule**

**Data Analyst | Python | SQL | Power BI | Excel | Generative AI | Machine Learning**

---

## ⭐ Project Highlights

```text
15,000          Original Records
14,884          Cleaned Records
39              Features
94.48%          Gradient Boosting R² Score
9.49%           Fraudulent Claim Rate
3               Customer Risk Segments
```

---

## ⭐ If you found this project useful

Feel free to ⭐ star the repository and explore the notebook for the complete analysis, machine learning workflow, and business insights.
