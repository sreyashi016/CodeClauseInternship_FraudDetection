<p align="center">
  <img src="FraudDetection.jpg" alt="Sentiment Analysis Output" width="600"/>
</p>

# 🔐 FRAUD DETECTION~

## 📑 TABLE OF CONTENTS

* 📘 Project Summary
* 📂 Dataset Details
* ⚙️ Workflow Summary
* 📈 Model Performance
* 📈 Results Snapshot
* 🛠 Tools & Libraries Used
* 👩‍💻 Author


---

This project demonstrates a **practical machine learning pipeline** for detecting fraudulent credit card transactions using the powerful **XGBoost classifier**. It showcases essential data preprocessing techniques, categorical encoding, scaling, and handling class imbalance — all aligned with a real-world fraud detection use case.

---

## 📘 PROJECT SUMMARY

The objective of this notebook is to classify financial transactions as **fraudulent** or **non-fraudulent**. The dataset contains both numerical and categorical features, and the modeling pipeline is crafted to ensure accuracy despite a highly **imbalanced target distribution**.

The project includes clear steps from raw data to model predictions, making it highly reproducible and educational.

---

## 📂 DATASET DETAILS
* **Name**:Fraud Detection Dataset
* **Source**:[Kaggle Dataset](https://www.kaggle.com/datasets/bhadramohit/credit-card-fraud-detection)
* **Size**: \~100,000+ rows
* **Features Include**:

  * `TransactionDate` (cleaned with custom logic)
  * `TransactionType` and `Location` (categorical)
  * `Amount` and other numerical attributes
* **Target Column**: Binary classification

  * `0` = Non-fraudulent
  * `1` = Fraudulent

---

## ⚙️ WORKFLOW SUMMARY

### 1. **Data Preprocessing**

* Removed nulls and duplicate entries
* Extracted and formatted `TransactionDate`
* Analyzed unique values in each column

### 2. **Feature Transformation**

* Applied **OneHotEncoding** to `TransactionType` and `Location`
* Scaled features using **StandardScaler**

### 3. **Train-Test Split**

* Used an 80/20 train-test split with `random_state=42` for reproducibility

### 4. **Modeling with XGBoost**

* Initialized `XGBClassifier` with `scale_pos_weight` to address imbalance
* Trained on the processed training data

### 5. **Evaluation**

* Evaluated predictions using:

  * **Accuracy Score**
  * **F1 Score**
  * **Confusion Matrix** (visualized using Seaborn)

### 6. **Final Prediction**

* Used a single, scaled test input to simulate real-time fraud detection
* Clearly displayed the result as either:

  * **"Fraudulent Transaction"** or
  * **"Non-Fraudulent Transaction"**

---
## 📈 MODEL PERFORMANCE
| Model                | Accuracy |
|---------------------|----------|
| XGBoost Classifier | ~92%     |

---

## 📈 RESULTS SNAPSHOT

* Model training was successful with good performance on evaluation metrics.
* Visualization of the confusion matrix helped in understanding false positives and negatives.
* The final test input predicted and labeled the nature of the transaction accurately.

---

## 🛠 TOOLS AND LIBRARIES USED

* **Python 3**
* `pandas`, `numpy` – Data manipulation
* `matplotlib`, `seaborn` – Visualization
* `scikit-learn` – Preprocessing & metrics
* `xgboost` – Core model
* `OneHotEncoder`, `StandardScaler`, `train_test_split` – Data preparation tools

---

## 👩‍💻 AUTHOR

**Sreyashi Choudhury**
A machine learning enthusiast passionate about applying data science to solve impactful problems.


