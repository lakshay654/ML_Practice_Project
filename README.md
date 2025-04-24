# 🛡️ System Threat Forecaster - IIT Madras ML Practice Project

This repository contains my submission for a **Machine Learning competition** conducted as part of the *"Machine Learning Practice"* course under the **IIT Madras Online BSc Degree in Data Science**.

---

## 📌 Objective

The aim of this project was to develop a **binary classification model** to predict whether a system is **infected by malware or not**, using a combination of system specifications and software configuration data.

---

## 📂 Project Overview

- **Problem Type**: Binary Classification
- **Target Variable**: Malware Infection (0 = Clean, 1 = Infected)
- **Evaluation Metric**: Accuracy
- **Tools Used**: Python, Pandas, Scikit-learn, XGBoost, LightGBM, Matplotlib, Seaborn

---

## 📊 Key Highlights

- 🔍 **Feature Engineering**: Transformation of version IDs, binning of high-cardinality features, correlation analysis, and removal of redundant/low variance features.
- 🧼 **Preprocessing**: Outlier handling, missing value imputation, and encoding (Ordinal > OneHot for tree-based models).
- 🧠 **Models Used**:
  - Logistic Regression
  - Random Forest
  - Support Vector Machine
  - LightGBM (Best performer: 62.98% Accuracy)
  - XGBoost
  - Ensembling: Voting & Stacking Classifiers
- 📈 **Final Accuracy**: Achieved up to **63.14%** using a **Voting Classifier** (XGBoost + LightGBM).

---

## 🧠 Key Insights

- Features like `IsSecureBootEnabled`, `ProcessorCoreCount`, `TotalPhysicalRAMMB` were most predictive.
- Features with no variance (e.g., `IsBetaUser`) or almost unique values (e.g., `MachineID`) were dropped.
- Balanced target distribution (~50/50) allowed use of accuracy as a reliable metric.
