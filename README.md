# ☄️ Hazardous Asteroid Detection using Machine Learning

![ML](https://img.shields.io/badge/Machine%20Learning-Classification-blue)
![Status](https://img.shields.io/badge/Project-Finished-green)
![Python](https://img.shields.io/badge/Python-3.8+-yellow)

---

## 📌 Overview

This project builds a **binary classification system** to predict whether a Near-Earth Object (NEO) is potentially hazardous to Earth using NASA asteroid data.

It focuses on:
- Class imbalance handling (hazardous objects are rare)
- Trade-off between **Precision vs Recall**
- Model benchmarking for safety-critical prediction

---

## 📊 Dataset Features

- **Estimated Diameter** (km)
- **Relative Velocity** (km/s)
- **Miss Distance** (km)
- **Absolute Magnitude**
- **Target:** Hazardous (True/False)

---

## 🛠️ Methodology

### 1. Data Preprocessing
- Cleaned and validated dataset (no missing values)
- Applied **StandardScaler** for feature normalization
- Encoded categorical/boolean variables

### 2. Exploratory Data Analysis (EDA)
- Performed IQR analysis (outliers retained due to domain importance)
- Found strong correlation between:
  - Absolute Magnitude
  - Hazardous label

### 3. Class Imbalance Handling
- Used **SMOTE** to balance training data
- Improved minority class learning

### 4. Models Implemented
- Linear Perceptron (baseline)
- K-Nearest Neighbors (k=1 to 10 tuning)
- Decision Tree (feature importance + high recall behavior)

---

## 📈 Results

| Model | Accuracy | Precision | Recall |
|------|----------|-----------|--------|
| Perceptron | 78% | 0.29 | 0.96 |
| KNN (k=5) ⭐ | **87%** | **0.35** | 0.80 |
| KNN (k=9) | 83% | 0.33 | 0.83 |
| Decision Tree | 78% | 0.30 | **0.98** |

---

## 🔍 Key Insights

- **Best Model:** KNN (k=5) → best balance of accuracy and precision-recall trade-off
- **Critical Feature:** Absolute Magnitude strongly influences hazard prediction
- **Safety Insight:** High recall is crucial in planetary defense systems

---

## 🚀 How to Run

```bash
git clone https://github.com/your-username/asteroid-detection.git
cd asteroid-detection

pip install -r requirements.txt
python asteroid_detection.py
```

---

## 📦 Requirements

```
numpy
pandas
matplotlib
seaborn
scikit-learn
imbalanced-learn
```

---

## 🧠 Conclusion

This project demonstrates how machine learning can assist in **planetary defense systems**, where missing a hazardous object is far more critical than raising a false alarm.

---

## 👨‍💻 Author

**P. Sai Dharanidhar Ram**  
Indian Institute of Technology (IIT) Kharagpur  
Artificial Intelligence & Machine Learning
