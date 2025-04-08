# 📊 Colorectal Cancer Survival Prediction

## 🧾 Introduction
This project focuses on predicting colorectal cancer patient outcomes using different machine learning algorithms such as Logistic Regression, Random Forest Classifier, XGBoost, CatBoost, and Linear SVM. It involves data preprocessing, exploratory data analysis (EDA), feature engineering, model training, and evaluation to assist in clinical decision-making and survival analysis.

---

## 🧪 Exploratory Data Analysis (EDA)

- **Class Distribution:** Severe class imbalance observed between *Survived* and *Deceased* patients.
- **Correlation Analysis:** Identified strong correlations between survival and several clinical features (e.g., tumor size, lymph node involvement).
- **Distribution Plots:** Visualized skewed distributions in key features; normalization was considered.
- **Categorical vs Target:** Bar plots showed how different categories (like stages, treatment types) relate to survival.

---

## ⚙️ Data Preprocessing & Feature Engineering

- **Handling Missing Values:** Imputation strategies were used to fill in missing data.
- **Encoding:** Categorical variables encoded using OneHot and Label Encoding.
- **Balancing Data:** SMOTE was applied to address class imbalance in the training set.
- **Feature Scaling:** StandardScaler used to normalize the features.

---

## 🤖 Model Training & Evaluation

Multiple models were trained and compared:

### 🔍 Models Evaluated
| Model               | Accuracy | F1 Score | Notes |
|--------------------|----------|----------|-------|
| **Logistic Regression** | Fair     | Low for minority class | Fast & interpretable |
| **Random Forest**       | Good     | Balanced   | Handles non-linear relationships |
| **XGBoost**             | Very Good| Strong F1  | Balanced class performance |
| **CatBoost**            | Best F1  | Strong F1 | Poor recall on minority class |
| **Linear SVC**          | Weak     | Low        | Fast but sensitive to imbalance |

- **CatBoost** had the highest F1 score.
- **XGBoost** provided the best trade-off between accuracy and class balance.
- **Linear models** (Logistic Regression, LinearSVC) were computationally efficient but struggled with the imbalance.

---

## 📈 Visualizations

- **Confusion Matrices** and **ROC curves** provided insight into each model’s strengths and weaknesses.
- **Feature Importance** plots helped explain model decisions and the relevance of clinical features.

---

## ✅ Conclusion & Recommendations

- **CatBoost** excels in F1 Score.
- **XGBoost** provided a balanced performance and practical deployment.
- **Linear models** can be used for baseline or in low-resource environments.

- Future improvements include:
  - Use a better dataset about Colorectal Cancer
  - Trying other ensemble methods
  - Optimizing hyperparameters more
  - Testing anomaly detection for rare class handling
  - Incorporating clinical expert feedback for feature selection
