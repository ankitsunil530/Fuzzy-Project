# Fuzzy Logic-Based Diabetes Diagnosis System

## Overview  
This project implements a *fuzzy inference system (FIS)* for diagnosing diabetes risk based on clinical input data (such as glucose level, BMI, and age). The system uses **Mamdani fuzzy logic**, linguistic rules, and intuitive membership functions to provide an interpretable risk score (low / medium / high) rather than a simple binary classification.

## Motivation  
Traditional binary classification models (e.g., “diabetic” vs “non-diabetic”) may lack interpretability and struggle with uncertain or gradual transitions in medical data. Fuzzy logic handles uncertainty and offers rule-based explanations, making it suitable for a decision-support tool in medical settings.

## Key Features  
- Uses the [Pima Indians Diabetes Dataset](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database) for prototyping.  
- Inputs:  
  - **Glucose (mg/dL)**  
  - **BMI (kg/m²)**  
  - **Age (years)**  
- Output:  
  - **Diabetes risk score** (0–100), categorized as *Low / Medium / High*.  
- Membership functions designed for each input and output.  
- Rule base with intuitive IF-THEN statements (e.g., *IF glucose is high AND BMI is overweight THEN risk is high*).  
- Implementation using Python and [scikit-fuzzy](https://github.com/scikit-fuzzy/scikit-fuzzy).  
- Evaluation with standard metrics (accuracy, precision, recall, F1-score) and ROC curve.  
- Optional: Hardware demo using Arduino to illustrate fuzzy microcontroller implementation of the same logic.

## Getting Started  
### Prerequisites  
- Python 3.x  
- Libraries: `numpy`, `pandas`, `matplotlib`, `scikit-learn`, `scikit-fuzzy`  
  ```bash
  pip install numpy pandas matplotlib scikit-learn scikit-fuzzy
