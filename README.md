# Customer Churn Prediction & Customer Segmentation

An end-to-end Machine Learning project that predicts customer churn using a **Random Forest Classifier** and segments customers into meaningful groups using **K-Means Clustering**. The project analyzes customer behavior, identifies factors contributing to churn, and provides actionable customer segments to support business decision-making.

---

## 📌 Project Overview

Customer churn is a major challenge for subscription-based businesses. Identifying customers who are likely to leave and understanding their behavior enables companies to implement targeted retention strategies.

This project follows a complete machine learning workflow:

* Perform Exploratory Data Analysis (EDA)
* Preprocess customer data
* Build and evaluate a Random Forest classifier for churn prediction
* Calculate churn probability for each customer
* Segment customers using K-Means Clustering
* Visualize customer segments and derive business insights

---

## 📂 Dataset

The project uses the **Telco Customer Churn** dataset containing customer information such as:

* Customer demographics
* Tenure
* Monthly Charges
* Total Charges
* Contract Type
* Internet Service
* Payment Method
* Tech Support
* Customer Lifetime Value (CLTV)
* Churn information

**Target Variable**

* `Churn Value`

  * `1` → Customer churned
  * `0` → Customer retained

---

## 🛠️ Tech Stack

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn

---

## 📈 Project Workflow

### 1. Exploratory Data Analysis (EDA)

The dataset is explored to understand customer behavior through various visualizations and statistical analysis.

Visualizations include:

* Distribution of Tenure Months
* Distribution of Monthly Charges
* Tenure vs Churn
* Monthly Charges vs Churn
* Contract Type vs Churn
* Internet Service vs Churn
* Payment Method vs Churn
* Tech Support vs Churn
* Correlation Analysis

---

### 2. Data Preprocessing

The following preprocessing steps are performed:

* Convert `Total Charges` to numeric values
* Handle missing values
* Remove irrelevant columns
* Encode categorical variables using One-Hot Encoding
* Split data into training and testing sets

---

### 3. Customer Churn Prediction

A **Random Forest Classifier** is trained to predict customer churn.

Three models are developed:

* Basic Random Forest
* Balanced Random Forest
* Tuned Random Forest

The tuned model is used as the final prediction model.

---

### 4. Model Evaluation

The model is evaluated using:

* Accuracy Score
* Confusion Matrix
* Precision
* Recall
* F1-Score
* ROC Curve
* AUC Score

---

### 5. Feature Importance

Random Forest feature importance is used to identify the variables that contribute the most to customer churn.

Less important features are removed to simplify the model.

---

### 6. Customer Segmentation

Instead of clustering customers only on demographic information, the project combines business features with the model's predicted churn probability.

Features used for clustering:

* Tenure Months
* Monthly Charges
* Total Charges
* Predicted Churn Probability

The features are standardized using **StandardScaler** before clustering.

---

### 7. K-Means Clustering

The **Elbow Method** is used to determine the optimal number of clusters.

The final model creates **3 customer segments**.

| Cluster | Segment                 | Description                                                                 |
| ------- | ----------------------- | --------------------------------------------------------------------------- |
| 0       | Budget Loyal Customers  | Long-term customers with lower monthly spending and low churn probability   |
| 1       | High Risk Customers     | Customers with high predicted churn probability requiring retention efforts |
| 2       | Loyal Premium Customers | High-value customers with higher spending and strong loyalty                |

---

### 8. Data Visualization

Customer segments are visualized using scatter plots:

* Tenure Months vs Churn Probability
* Monthly Charges vs Churn Probability

These visualizations help distinguish different customer groups.

---

## 📊 Results

* Successfully predicted customer churn using Random Forest.
* Identified the most influential features affecting churn.
* Segmented customers into three meaningful business groups.
* Combined supervised and unsupervised learning to provide actionable business insights.

---

## 🚀 Future Improvements

* Compare multiple classification algorithms (XGBoost, LightGBM, Logistic Regression)
* Hyperparameter tuning using GridSearchCV
* Handle class imbalance using SMOTE
* Deploy the model using Flask, FastAPI, or Streamlit
* Build an interactive dashboard for business users

---

## 📁 Project Structure

```text
Customer-Segmentation/
│
├── CUSTOMER_SEGMENTATION_PROJECT.ipynb
├── Telco_customer_churn.xlsx
├── README.md
└── requirements.txt
```

---

## ▶️ How to Run

1. Clone the repository.

```bash
git clone https://github.com/your-username/customer-segmentation.git
```

2. Navigate to the project directory.

```bash
cd customer-segmentation
```

3. Install the required dependencies.

```bash
pip install -r requirements.txt
```

4. Open the Jupyter Notebook or Google Colab notebook.

5. Run all cells sequentially.

---

## 📌 Key Learning Outcomes

* Exploratory Data Analysis (EDA)
* Data Preprocessing
* Feature Engineering
* Random Forest Classification
* Feature Importance Analysis
* ROC-AUC Evaluation
* Customer Churn Prediction
* Standardization
* K-Means Clustering
* Customer Segmentation
* Data Visualization

---

## 📄 License

This project is intended for educational and learning purposes.
