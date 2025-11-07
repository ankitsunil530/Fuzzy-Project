---
# 🩺 Fuzzy Logic-Based Diabetes Diagnosis System

## 📘 Overview  
This project implements a **Mamdani Fuzzy Inference System (FIS)** for diagnosing diabetes risk using clinical parameters — **Glucose**, **BMI**, and **Age**.  
It uses fuzzy logic to handle uncertainty in medical data and produce interpretable outputs such as **Low**, **Medium**, and **High risk** of diabetes.  
The system is inspired by the research paper:  
> *A Fuzzy Rule-Based System for Classification of Diabetes*, Sensors (MDPI), 2021.

---

## 🎯 Objective  
To develop an **intelligent, explainable, and data-driven** model that predicts diabetes risk using fuzzy logic, improving interpretability compared to black-box machine learning models.

---

## ⚙️ Technologies Used
- **Language:** Python 3.x  
- **Libraries:** `numpy`, `pandas`, `matplotlib`, `scikit-fuzzy`, `scikit-learn`  
- **Dataset:** [Pima Indians Diabetes Dataset](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database)

---

## 🧩 Fuzzy System Design  

### Input Variables  
| Variable | Range | Linguistic Labels |
|-----------|--------|------------------|
| Glucose | 0 – 200 | Low, Normal, High |
| BMI | 0 – 60 | Underweight, Normal, Overweight |
| Age | 20 – 80 | Young, Middle-aged, Old |

### Output Variable  
| Variable | Range | Linguistic Labels |
|-----------|--------|------------------|
| Diabetes Risk | 0 – 100 | Low, Medium, High |

---

## 🔢 Fuzzy Rule Base  
Sample rules used in the system:
```

1. IF Glucose IS High THEN Risk IS High
2. IF Glucose IS Normal AND BMI IS Overweight THEN Risk IS Medium
3. IF Glucose IS Low AND BMI IS Normal THEN Risk IS Low
4. IF Glucose IS High AND Age IS Old THEN Risk IS High
5. IF BMI IS Normal AND Age IS Young THEN Risk IS Low

````

A total of **12–15 rules** were implemented for the Mamdani inference system.

---

## 🧠 Implementation Steps
1. **Dataset Loading & Preprocessing**
   - Imported Pima Indians dataset.  
   - Normalized features (Glucose, BMI, Age).  

2. **Membership Function Design**
   - Defined triangular and trapezoidal MFs using `skfuzzy.trimf` and `trapmf`.  
   - Visualized all input/output fuzzy sets.

3. **Rule Formation & Inference**
   - Constructed linguistic rules using `ctrl.Rule`.  
   - Built Mamdani control system and simulated outputs.

4. **Defuzzification & Output**
   - Used **centroid defuzzification** to compute crisp diabetes risk values.  

5. **Evaluation**
   - Compared fuzzy output against dataset labels using thresholding.
   - Calculated **Accuracy, Precision, Recall, and F1-Score**.

---

## 📊 Experimental Results  

| Metric | Fuzzy System | Logistic Regression |
|--------|---------------|--------------------|
| Accuracy | 0.73 | 0.78 |
| Precision | 0.65 | 0.67 |
| Recall | 0.55 | 0.59 |
| F1-Score | 0.56 | 0.60 |

The fuzzy system provides slightly lower numerical accuracy but **superior interpretability** and explainable decision rules.

---

## 🧾 Sample Output
```bash
Input → Glucose = 150, BMI = 30, Age = 45  
Predicted Risk = 74.2 → "High Risk"
````

The FIS generates visual plots for:

* Membership functions
* Rule evaluation surface
* ROC curve and confusion matrix

---

## 💡 Key Insights from Research Paper (Sensors, 2021)

* Proposed two fuzzy classifiers trained on **768 Pima Indians records** (52% training, 48% testing).
* Achieved up to **96.47% accuracy**, **95.76% recall**, and **93.39% precision**.
* Demonstrated fuzzy logic’s strength in **handling vagueness and medical uncertainty**.
* Motivated the use of **simple features (Glucose, BMI, Age)** for early diabetes screening.

---

## 🧰 Installation & Usage

```bash
git clone https://github.com/ankitsunil530/Fuzzy-Project.git
cd Fuzzy-Project
pip install numpy pandas matplotlib scikit-learn scikit-fuzzy
python fuzzy_diabetes.py
```

---

## 🔬 Future Scope

* Extend model with more clinical parameters (Blood Pressure, Insulin).
* Integrate with **Arduino microcontroller** to control LEDs (Low/Medium/High risk).
* Explore **Type-2 fuzzy systems** or **Neuro-Fuzzy (ANFIS)** for adaptive learning.
* Develop a **web interface** for real-time diabetes screening.

---

## 📄 Reference

> **K.M. Aamir et al.**, *A Fuzzy Rule-Based System for Classification of Diabetes*, Sensors, 21(8095), MDPI, 2021.
> DOI: [10.3390/s21080895](https://doi.org/10.3390/s21080895)

---
## 👥 Team Members
- **Sunil Kumar** — Project Lead, Fuzzy Logic System Design & Implementation  
- **Komal Singh** — Data Preprocessing, Evaluation & Documentation  
- **Mayank Deshmukh** — Rule Base Development & Visualization


## 👨‍💻 Author

**Sunil Kumar**
3rd Year B.Tech CSE @ IIITDM Jabalpur
🔗 [GitHub Profile](https://github.com/ankitsunil530)

```



