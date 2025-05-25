# Student Performance Prediction with Machine Learning

This project explores a real-world dataset of 5,000 students collected from a private learning provider. The goal is to analyze patterns in academic performance and build machine learning models to predict student outcomes based on behavioral, demographic, and academic features.

---

## Dataset Overview

The dataset includes the following types of information:
- Academic scores: Midterm, Final, Assignments, Quizzes, Participation
- Behavioral: Attendance, Study Hours, Sleep, Stress Level
- Demographics: Gender, Age, Department, Parental Education, Family Income
- Includes both a **masked** version and a **biased** version for challenge

---

## Project Highlights

- **EDA & Preprocessing**: Missing value handling, one-hot encoding, feature selection
- **Classification Models**:
  - Tried KNN, Random Forest, Logistic Regression, and XGBoost
  - Accuracy for grade prediction was low (~35%) due to bias and label noise
- **Regression Models**:
  - Shifted to predicting `Total_Score` instead of `Grade`
  - Best model: **Random Forest Regressor** with MAE ≈ 12
  - Compared SVR and XGBoost but found RF most effective

---

## Models Compared

| Model                    | Task        | MAE   | R² Score |
|-------------------------|-------------|-------|----------|
| Random Forest Regressor | Regression  | 12.00 | ~0.00     |
| XGBoost Regressor       | Regression  | 12.98 | -0.05    |
| SVR (SVM Regressor)     | Regression  | 14.11 | -0.28    |
| KNN / RF Classifier     | Classification (Grade) | ~35% Accuracy | — |

---

## Files

- `Student_Performance_Analysis.ipynb` → Main Kaggle notebook
- `data/Students_Grading_Dataset.csv` → Masked version
- `data/Students_Grading_Dataset_Biased.csv` → Biased version
- `images/` → Charts or confusion matrix screenshots (optional)

---

## Key Learnings

- Subjective labels (grades) are hard to predict using ML without rich contextual data.
- Regression on total score yields better performance.
- Feature selection and simple models can outperform more complex methods.

---

## How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/yuhengzhai/student-performance-prediction.git
   cd student-performance-prediction
