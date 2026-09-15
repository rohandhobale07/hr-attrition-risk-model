                                 👨‍💼📉 Attrition Risk Model — HR Analytics 📉👨‍💼

A classification-based machine learning project designed to identify at-risk employees early, using class-imbalance correction to catch far more true attrition cases than a naive baseline model.

📌 Project Overview

This project analyzes HR department data using Python and Scikit-Learn to predict employee attrition and uncover the behavioral and tenure-related factors driving it.

The project contains **1,470 employee records across 35 features**, including distance from home, manager tenure, and total working years.

The analysis focuses on exploratory analysis, benchmarking classification models, and specifically diagnosing and fixing a class-imbalance problem that was hiding the model's real weakness.

🎯 Project Objectives

- Perform EDA to uncover attrition patterns and behavioral drivers
- Visualize key relationships via KDE plots and correlation heatmaps
- Benchmark multiple classification models on the same train/test split
- Diagnose why a high-accuracy model was still missing most at-risk employees
- Correct class imbalance to materially improve real-world detection
- Quantify the accuracy-vs-recall trade-off explicitly, not just report one metric

🛠️ Technologies Used

🐍 Python
- Data analysis and modeling

📊 Pandas & NumPy
- Data cleaning and feature handling

📈 Matplotlib & Seaborn
- KDE plots and correlation heatmaps

🤖 Scikit-Learn
- Logistic Regression, Random Forest, Decision Tree classifiers

📓 Jupyter Notebook
- Exploratory analysis and model development

📁 Dataset

- 📊 1,470 employee records
- 🧩 35 features per employee
- 🔑 Key fields: Distance From Home, Years With Current Manager, Total Working Years, Attrition (target variable)

🔍 Exploratory Data Analysis

- Uncovered a **16.1% attrition rate** across the workforce
- Identified top attrition drivers: distance from home, years with current manager, total working years
- Visualized relationships via KDE plots and correlation heatmaps

🤖 Model Benchmarking

Trained and compared 3 classification models on a 70/30 train-test split:

- Logistic Regression
- Random Forest
- Decision Tree

⚠️ The Hidden Problem

The best baseline model (Logistic Regression) achieved **87.5% accuracy** — but only **40% recall** on employees who actually left. In plain terms: it looked accurate, but it was missing 6 out of every 10 employees who were genuinely at risk.

🛠️ The Fix

Retrained using **balanced class weights** to directly address the imbalance between "stayed" and "left" employees in the training data.

📈 Result

Recall on departing employees improved **from 40% to 70%** — a deliberate trade-off of 12 accuracy points in exchange for catching far more employees who were actually at risk of leaving.

💡 Key Business Insights

- A model can look accurate on paper while still failing at the thing that actually matters (catching at-risk employees)
- Distance from home and manager tenure are meaningful, actionable attrition signals
- Accuracy alone is a misleading metric on imbalanced classification problems — recall matters more here

⭐ Project Highlights

📊 Employees Analyzed: 1,470

🧩 Features: 35

📉 Attrition Rate: 16.1%

🤖 Models Compared: 3

📈 Baseline Accuracy: 87.5%

⚠️ Baseline Recall (at-risk employees): 40%

✅ Recall After Fix: 70%

⚖️ Trade-off Accepted: −12 accuracy points for +30 recall points

