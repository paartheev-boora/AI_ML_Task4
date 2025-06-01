#  Breast Cancer Prediction using Logistic Regression

This project uses **Logistic Regression** on the Breast Cancer Wisconsin dataset to classify tumors as **malignant** or **benign**, with an emphasis on **model interpretability**, **threshold tuning**, and **performance metrics**.

---

##  Dataset

- Source: [Kaggle Dataset](https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data)
- Features include radius, texture, perimeter, area, smoothness, and other cell nucleus characteristics.
- Target variable: `diagnosis` (Malignant = 1, Benign = 0)

---

##  Steps in the Project

### 1. **Data Import & Preprocessing**
- Loaded data from `dataA.csv`
- Dropped irrelevant columns: `id`, `Unnamed: 32`
- Converted `diagnosis` from categorical to numerical (M → 1, B → 0)

### 2. **Train-Test Split & Scaling**
- Used an 80/20 train-test split.
- Standardized features using `StandardScaler` to ensure fair learning.

### 3. **Model Training**
- Applied `LogisticRegression` from `sklearn` with `max_iter=10000`.
- Achieved **accuracy of ~97.4%** on the test set.

### 4. **Model Evaluation**
- Evaluated using:
  - **Accuracy**: 97.4%
  - **Precision**: 97.6%
  - **Recall**: 95.3%
  - **F1 Score**: 96.4%
  - **ROC-AUC**: 0.997

- Plotted and interpreted the **confusion matrix**.

### 5. **Threshold Tuning & Sigmoid Explanation**
- Explained the **sigmoid function**, used to convert linear output into probabilities.
- Explored how different **classification thresholds** (not just 0.5) affect model behavior.
- Calculated precision, recall, and F1 across 100 thresholds.
- Chose **optimal threshold = 0.38** based on maximum F1 score.

### 6. **Improved Evaluation at Tuned Threshold**
- New performance:
  - **Precision**: 97.7%
  - **Recall**: 97.7%
  - **F1 Score**: 97.7%
- Displayed updated confusion matrix.

---

## 📈 Key Insights

- Logistic Regression performs very well on this dataset.
- Threshold tuning improves control over false positives vs. false negatives.
- ROC-AUC close to 1.0 shows excellent model separability.

---
