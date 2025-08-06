# 🧠 Ensemble Learning with Decision Trees: Bagging & Boosting

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-%23F37626.svg?style=for-the-badge&logo=Jupyter&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-ffffff?style=for-the-badge&logo=matplotlib&logoColor=black)
![Scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)

![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)



## 🚀 Project Highlights (TL;DR)

- 📚 **Objective:** Apply and evaluate ensemble learning techniques (Bagging & Boosting) on real-world classification problems.
- 🌲 **Base model:** Decision Trees, chosen for their variance and interpretability.
- 🧪 **Datasets used:**
  - Online Shoppers’ Purchasing Intention (binary classification)
  - Student Dropout & Academic Success (multiclass classification)
- 🔍 **Key Focus:** 
  - Compare bias, variance, and accuracy across models
  - Apply Grid Search & Cross-Validation
  - Analyze performance tradeoffs
- 📊 **Results:** Tuned ensemble models improved accuracy up to **+83%**, while reducing variance and overfitting in several scenarios.

---

## 🔍 Overview
This project showcases how ensemble learning techniques such as **Bagging** and **Boosting** can improve prediction performance when applied to classification problems. Two real-world datasets are used to demonstrate these methods using **Decision Trees** as base learners.

The goal is to analyze how ensemble models compare to a single Decision Tree in terms of **accuracy**, **bias**, and **variance**, and to simulate a real-world workflow through hyperparameter tuning and cross-validation.

---

## 🎯 Objective

To understand and implement ensemble methods (Bagging and Boosting) using Decision Trees as base classifiers, and compare their performance against a single tree model. Evaluation includes:
- Accuracy
- Bias-Variance Decomposition
- Generalization across multiple validation/test splits
- Hyperparameter tuning via GridSearchCV

---

## 🧰 Techniques Used

- **Decision Tree Classifier**
- **Bagging Classifier** (`BaggingClassifier` from `sklearn`)
- **Boosting** (AdaBoost with `AdaBoostClassifier`)
- **Bias-Variance Decomposition** (via `mlxtend`)
- **Cross-validation** (with varying folds)
- **GridSearchCV** for model tuning
- Performance evaluation using accuracy, MSE, bias² and variance

---

## 📚 Project Structure

This project is structured in two phases:

### 🔹 Dataset 1 – *Online Shoppers Purchasing Intention*
A simplified case used to introduce ensemble learning concepts and compare basic performance of Bagging and Boosting vs. a base Decision Tree using:
- One train/test split
- Bias-Variance analysis

### 🔹 Dataset 2 – *Student Dropout and Academic Success*
A more advanced and realistic workflow including:
- Train/Validation/Test splits
- GridSearchCV tuning for Bagging and Boosting
- Bias-Variance analysis across validation and test sets
- Cross-validation with different fold sizes

---

## 📂 Datasets

### 1. **Online Shoppers Purchasing Intention**
- Binary classification: will the user complete a purchase?
- Features: 17 (10 numerical, 8 categorical)
- Instances: 12,330
- Target: `Revenue` (True/False)

Source: [Kaggle](https://www.kaggle.com/datasets/rohitsahoo/predicting-online-shoppers-intention)

### 2. **Student Dropout and Academic Success**
- Multi-class classification: Dropout / Enrolled / Graduate
- Features: 36
- Instances: 4,424
- Target: `Target` (3 classes)

Source: [UCI Repository](https://archive.ics.uci.edu/ml/datasets/Student+Performance)

---

## 📈 Key Results

### 📊 Dataset 1: Online Shoppers

| Model               | Accuracy | Bias²  | Variance |
|--------------------|----------|--------|----------|
| Decision Tree       | 85.9%    | 0.078  | 0.040    |
| Bagging Classifier  | 88.5%    | 0.087  | 0.022    |
| Boosting Classifier | 85.7%    | 0.084  | 0.036    |

➡️ Bagging significantly reduced variance; Boosting improved bias using a high-bias base learner.

### 📊 Dataset 2: Student Dropout

| Model                        | Dataset Split | Accuracy | Bias²  | Variance |
|-----------------------------|----------------|----------|--------|----------|
| Decision Tree               | Validation     | 0.6416   | 0.3521 | 0.2930   |
| Bagging (default)           | Validation     | 0.7009   | 0.3847 | 0.1590   |
| Boosting (default)          | Validation     | 0.6575   | 0.3531 | 0.2925   |
| Bagging (tuned)             | Validation     | 0.7306   | 0.4218 | 0.1106   |
| Decision Tree               | Test           | 0.6921   | 0.2926 | 0.2869   |
| Bagging (tuned + test set)  | Test           | 0.8292   | 0.3909 | 0.0608   |
| Boosting (tuned)            | Validation     | 0.7352   | 0.4106 | 0.0990   |
| Boosting (tuned + test set) | Test           | 0.7674   | 0.3570 | 0.0634   |

---

## 💡 Insights

- Bagging was particularly effective in reducing variance and improving generalization.
- Boosting showed its strength in correcting bias when used with a high-bias base learner.
- Hyperparameter tuning had a significant impact on test performance.
- Cross-validation confirmed the models’ ability to generalize across different splits.

---

## 📌 Notes

This is a **portfolio project**. It is not intended for clinical use and should not be used for real-world medical decision-making.

---

## 📧 Contact

**Alessandro Conte**
[LinkedIn](https://www.linkedin.com/in/alessandro-conte-ds)
[GitHub](https://github.com/AlessandroConte)

---

## 📄 License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.

---
