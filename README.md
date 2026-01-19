# 📉 Customer Churn Prediction with Interactive App

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jitender2622/Customer-churn-prediction/blob/main/Customer_churn_prediction.ipynb)

This project builds a Machine Learning model to predict **Customer Churn** (whether a customer will cancel their service) for a Telecom company. It includes a complete data processing pipeline, handles class imbalance using SMOTE, and features an **interactive web interface** using Gradio for real-time predictions.

## 📄 Project Overview

Customer retention is critical for any subscription-based business. This tool helps identify "at-risk" customers based on their usage patterns and payment history, allowing companies to take proactive measures.

**Key Features:**
* **Data Analysis:** Visualization of churn distribution and feature correlations.
* **Imbalance Handling:** Uses **SMOTE** (Synthetic Minority Over-sampling Technique) to fix the imbalance between loyal and churning customers.
* **Model:** Trains a **Random Forest Classifier** for robust predictions.
* **Interactive UI:** A **Gradio** web app that allows users to adjust sliders (Charges, Tenure) and see the churn risk immediately.

## 📊 The Dataset

The project uses the [Telco Customer Churn dataset](https://github.com/IBM/telco-customer-churn-on-icp4d).
* **Target Variable:** `Churn` (Yes/No)
* **Features:** Tenure, Monthly Charges, Total Charges, Contract Type, Payment Method, etc.

## 🛠 Tech Stack

* **Python 3.x**
* **Pandas & NumPy:** Data Manipulation.
* **Scikit-Learn:** Model building and preprocessing.
* **Imbalanced-Learn (SMOTE):** For resampling training data.
* **Matplotlib & Seaborn:** For Exploratory Data Analysis (EDA).
* **Gradio:** For building the front-end web interface.

## ⚙️ Methodology

1.  **Preprocessing:**
    * Handled missing values in `TotalCharges`.
    * Encoded categorical variables (Gender, Payment Method, etc.) using `LabelEncoder`.
2.  **Visualization:**
    * Plotted class distribution to visualize the imbalance.
    * 

[Image of Class Distribution Chart]

    * Generated a Heatmap to understand feature correlations.
    * 
3.  **Training:**
    * Split data into 80% Training and 20% Testing.
    * Applied **SMOTE** to the training set to ensure the model learns both classes equally.
    * Trained a **Random Forest Classifier** (100 estimators).
4.  **Deployment:**
    * Wrapped the prediction logic in a `predict_churn` function.
    * Launched a Gradio interface with sliders for key inputs.

## 🚀 How to Run

### Option 1: Google Colab (Recommended)
Click the "Open in Colab" badge at the top. The notebook installs all necessary dependencies automatically.

### Option 2: Local Installation
1.  Clone the repository:
    ```bash
    git clone [https://github.com/jitender2622/Customer-churn-prediction.git](https://github.com/jitender2622/Customer-churn-prediction.git)
    ```
2.  Install dependencies:
    ```bash
    pip install pandas numpy scikit-learn imbalanced-learn matplotlib seaborn gradio
    ```
3.  Run the notebook or script.

## 📈 Model Performance

* **Accuracy:** ~77%
* **Precision/Recall:** The Classification Report (included in the notebook outputs) provides detailed metrics for both churners and non-churners.

## 🖥️ Interactive Demo

The notebook launches a Gradio app at the end.
* **Inputs:** Monthly Charges, Total Charges, Tenure.
* **Output:** Prediction (High Risk/Low Risk) with a confidence percentage.

![Gradio Interface Preview](https://gradio.app/assets/img/header-image.jpg) *Note: This link will be generated dynamically when you run the notebook.*

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
