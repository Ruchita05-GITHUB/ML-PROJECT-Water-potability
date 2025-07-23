# 💧 Water Potability and Irrigation Suitability Prediction

A Machine Learning project that predicts **whether a water sample is safe for drinking** (potable) and if not, whether it is **suitable for irrigation**, supporting both **public health** and **water conservation**.

---



## 🌍 Motivation

- 🌊 Water pollution is a global issue impacting **health, agriculture, and the environment**.
- 👶 Unsafe water causes diseases like cholera and typhoid, especially in rural areas.
- 🌾 Clean water isn’t always needed for drinking — reusing for **irrigation** reduces waste.
- ✅ Early prediction of water quality enables **timely action** to protect health and improve resource planning.

---

## 🎯 Project Objectives

1. Predict whether a water sample is **potable (safe for drinking)**
2. If not potable, assess if it is **suitable for irrigation**
3. Reduce water testing costs by using ML
4. Support **sustainable water resource management**

---

## 🔬 Features Used

- pH
- Hardness
- Solids
- Chloramines
- Sulfate
- Conductivity
- Organic_carbon
- Trihalomethanes
- Turbidity

---

## 🧠 Machine Learning Models Used

| Model                | Train Accuracy (%) | Test Accuracy (%) |
|---------------------|--------------------|-------------------|
| K-Nearest Neighbors | 75.71              | 62.77             |
| Decision Tree       | 70.30              | 64.90             |
| Random Forest       | 79.85              | **67.14**         |
| Naive Bayes         | 62.71              | 63.28             |
| Logistic Regression | 60.23              | 62.87             |
| XGBoost             | 69.91              | 64.50             |

✅ **Random Forest** gave the best results and was chosen as the final model due to:
- High accuracy
- Good feature importance insights
- Robustness to noise and missing values

---

## 🌿 Extended Feature: Irrigation Suitability Prediction

Even if water is **not potable**, it might be **usable for agriculture**.

### ✔️ How It Works:
- Based on key chemical parameters like:
  - pH
  - Hardness
  - Sulfate
  - Solids
  - Turbidity
- A **rule-based function** and **Random Forest model** classify if water is:
  - `1`: Suitable for irrigation
  - `0`: Not suitable

### ✅ Benefits:
- Encourages **efficient water reuse**
- Reduces **water waste** in agriculture
- Supports **sustainability goals**

---

## 🧪 Dataset

- Source: [Kaggle - Water Potability Dataset](https://www.kaggle.com/datasets/adityakadiwal/water-potability)
- 3,276 samples, 9 input features, and 1 target label (`Potability`)

---

## 📈 Performance Metrics Used

- **Accuracy**
- **Confusion Matrix**
- **Precision, Recall, F1-Score**
- All metrics were calculated using `classification_report` from `sklearn`.

---

## 📂 Project Structure

| File Name                | Description                                 |
|--------------------------|---------------------------------------------|
| `MLCODE.ipynb`           | Jupyter notebook with all code              |
| `water_potability.csv`   | Dataset                                     |
| `requirements.txt`       | Python dependencies                        |
| `.gitignore`             | Files ignored by Git                        |
| `README.md`              | Project summary (this file)                 |

---

## ▶️ How to Run

1. Install dependencies:
   ```bash
   pip install -r requirements.txt
