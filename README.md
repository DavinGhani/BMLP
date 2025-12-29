# Machine Learning Final Project: Customer Analytics 🚀

**Submission for Machine Learning Fundamentals Class**

This repository contains two distinct Machine Learning projects applied to a customer dataset. The project demonstrates proficiency in both **Supervised Learning** (Churn Prediction) and **Unsupervised Learning** (Customer Segmentation).

---

## 📂 Project Structure

The submission is divided into two main notebooks:

1.  **Classification (Supervised)**: Predicting customer churn.
    -   *File:* `[Klasifikasi]_Submission_Akhir_BMLP_Davin_Ghani.ipynb`
2.  **Clustering (Unsupervised)**: Segmenting customers into groups based on behavior.
    -   *File:* `[Clustering]_Submission_Akhir_BMLP_Davin_Ghani_AK.ipynb`

---

## 📊 Dataset Overview

Both projects utilize the same dataset: `data_D.csv`.

-   **Total Records**: 1000 entries_Submission_Akhir_BMLP_Davin_Ghani.ipynb].
-   **Key Features**: `CreditScore`, `Geography`, `Gender`, `Age`, `Tenure`, `Balance`, `NumOfProducts`, `HasCrCard`, `IsActiveMember`, `EstimatedSalary`.
-   **Target Variable**: `Churn` (Used only for the Classification task).

---

## 🤖 Part 1: Classification (Churn Prediction)

**Objective**: To build a model that accurately predicts whether a customer will stop using the service (`Churn` = 1) or stay (`Churn` = 0).

### Workflow
1.  **Data Preprocessing**:
    -   **Cleaning**: Removed non-predictive columns such as `Unnamed: 0` and `id`_Submission_Akhir_BMLP_Davin_Ghani.ipynb].
    -   **Encoding**: Applied `LabelEncoder` to categorical variables (`Gender`, `Geography`)_Submission_Akhir_BMLP_Davin_Ghani.ipynb].
    -   **Scaling**: Standardized numerical features using `StandardScaler` to optimize model performance_Submission_Akhir_BMLP_Davin_Ghani.ipynb].
    -   **Splitting**: Data split into 80% Training and 20% Testing sets_Submission_Akhir_BMLP_Davin_Ghani.ipynb].

2.  **Model Development**:
    Three algorithms were compared to find the best baseline:
    -   **Logistic Regression**
    -   **K-Nearest Neighbors (KNN)**
    -   **Random Forest Classifier**_Submission_Akhir_BMLP_Davin_Ghani.ipynb].

3.  **Optimization**:
    -   Hyperparameter tuning was performed on the **Random Forest** model using `GridSearchCV` to find the best parameters (e.g., `n_estimators`, `max_depth`)_Submission_Akhir_BMLP_Davin_Ghani.ipynb].

### Results
-   The models were evaluated using **Accuracy**, **Precision**, **Recall**, and **F1-Score**.
-   The tuned **Random Forest** model achieved the most stable performance on the test set_Submission_Akhir_BMLP_Davin_Ghani.ipynb].

---

## 👥 Part 2: Clustering (Customer Segmentation)

**Objective**: To identify distinct customer groups based on financial and behavioral patterns without using labeled data.

### Workflow
1.  **Feature Engineering**:
    -   Focused on numerical features such as `CreditScore`, `Age`, `Balance`, and `EstimatedSalary`_Submission_Akhir_BMLP_Davin_Ghani_AK.ipynb].
    -   Data was standardized using `StandardScaler`_Submission_Akhir_BMLP_Davin_Ghani_AK.ipynb].

2.  **Dimensionality Reduction**:
    -   **PCA (Principal Component Analysis)** was applied to reduce features into 2 principal components for better visualization and noise reduction_Submission_Akhir_BMLP_Davin_Ghani_AK.ipynb].

3.  **Optimal Cluster Selection**:
    -   **Elbow Method**: Used to visualize the inertia and find the "elbow" point.
    -   **Silhouette Score**: Calculated to validate the separation distance between clusters_Submission_Akhir_BMLP_Davin_Ghani_AK.ipynb].

4.  **Modeling**:
    -   Applied the **K-Means** algorithm using the optimal number of clusters ($K$) determined by the evaluation metrics_Submission_Akhir_BMLP_Davin_Ghani_AK.ipynb].

### Results
-   The customers were successfully segmented into distinct clusters.
-   The results were visualized using a 2D Scatter Plot based on PCA components_Submission_Akhir_BMLP_Davin_Ghani_AK.ipynb].

