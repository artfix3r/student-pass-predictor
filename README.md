# 🎓 Student Pass Predictor

A machine learning classification project that predicts whether a student will **pass or fail** based on study habits, attendance rate, and prior academic performance — without using the final score, simulating a real early-warning system.

---

## 📌 Problem Statement

Can we identify at-risk students **before their final exams** using behavioral and background features? This project builds and compares three classification models to answer that question.

---

## 📂 Dataset

- **Source:** [Student Academic Performance – 500 Students](https://www.kaggle.com/datasets/mubashirsidiki/student-academic-performance-500-students) (Kaggle)
- **Size:** 500 students, 11 features
- **Target Variable:** `passed` (Yes / No)

### Features Used

| Feature | Description |
|---|---|
| `study_hours_per_week` | Weekly study hours |
| `attendance_rate` | Percentage of classes attended |
| `previous_score` | Score from previous term |

> ⚠️ `final_score` was intentionally **dropped** to prevent data leakage — it directly determines whether a student passed and would not be available at prediction time.

---

## 🔧 Workflow

1. **Data Loading & Exploration** — `.info()`, `.describe()`, null checks, duplicate checks
2. **EDA** — Pairplot, histplot, scatterplot, countplot, correlation matrix
3. **Preprocessing** — Label encoding, dropping irrelevant/low-correlation features, StandardScaler
4. **Modeling** — Three classifiers trained and evaluated
5. **Evaluation** — Accuracy, Precision, Recall, F1-Score, Confusion Matrix

---

## 🤖 Models Compared

| Model | Accuracy |
|---|---|
| Logistic Regression | 97% |
| Random Forest | 100% |
| XGBoost | 100% |

> **Logistic Regression** performed best on this dataset, likely due to the relatively linear relationship between study hours and passing.

---

## 📊 Key Findings

- `study_hours_per_week` is the **strongest predictor** of passing (correlation: 0.65 with target)
- `attendance_rate` is the **second most important** feature
- `previous_score` has a weaker but still meaningful impact
- Demographic features (`gender`, `age`, `internet_access`) showed **very low correlation** with the outcome and were dropped

---

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/YOUR_USERNAME/student-pass-predictor.git
   ```

2. Install dependencies:
   ```bash
   pip install pandas numpy scikit-learn xgboost seaborn matplotlib
   ```

3. Open the notebook:
   ```bash
   jupyter notebook student-academic-performance.ipynb
   ```

---

## 🛠️ Tech Stack

- **Python 3.12**
- **pandas**, **numpy** — data manipulation
- **seaborn**, **matplotlib** — visualization
- **scikit-learn** — preprocessing, modeling, evaluation
- **XGBoost** — gradient boosting classifier

---

## 👤 Author

**Yusif İmamverdiyev**  


---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
