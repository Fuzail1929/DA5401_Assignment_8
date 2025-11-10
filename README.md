- Name : Mohd Fuzail
- Roll no. CH22B080
- Date : 10-11-2025


# 🚴‍♂️ Bike Sharing Demand Prediction using Ensemble Learning

- **Course:** DA5401 – Data Analytics Lab
- **Assignment:** A8 – Ensemble Learning for Complex Regression  
- **Dataset:** Bike Sharing Demand (Hourly)

---

## 📌 Objective
The aim of this project is to **predict hourly bike rental demand (`cnt`)** using weather and temporal features.  
We apply and compare **ensemble learning methods** to improve accuracy over traditional single models.

---

## 🗂 Dataset Details
| Feature Type | Example Features |
|-------------|----------------|
| Temporal | `hr`, `weekday`, `mnth`, `season` |
| Weather-related | `temp`, `hum`, `windspeed`, `weathersit` |
| Target | `cnt` (total number of rentals) |

We removed irrelevant fields:  
`instant`, `dteday`, `casual`, `registered`

Categorical features were **One-Hot Encoded**.

---

## 🔧 Methods Used

### 1. **Baseline Models**
| Model | Purpose |
|-------|---------|
| Decision Tree Regressor | Non-linear baseline model |
| Ridge / Lasso / ElasticNet Regression | Regularized linear baseline |

Best-performing baseline chosen using **RMSE**.

---

### 2. **Ensemble Learning Models**
| Technique | Goal | Model |
|----------|------|-------|
| **Bagging** | Reduce Variance | Bagging Regressor (Decision Tree base) |
| **Boosting** | Reduce Bias | Gradient Boosting Regressor |
| **Stacking** | Combine Model Strengths | KNN + Bagging + GB + Ridge (Meta-Learner) |

---

## 📊 Results

| Model | RMSE (↓ Lower is Better) |
|------|------:|
| Baseline Model | *varies* |
| Bagging Regressor | Improved over baseline |
| Gradient Boosting Regressor | **Better than Bagging & Baseline** |
| **Stacking Regressor** | **Best Performance Overall** ✅ |

---

## ✅ Conclusion
Ensemble Learning clearly outperformed single-model baselines.

- **Bagging** reduced variance and stabilized predictions.  
- **Boosting** reduced bias and improved accuracy significantly.  
- **Stacking** combined multiple learners and delivered the **lowest RMSE**, achieving the best generalization performance.

> **Final Insight:**  
> The **Stacking Regressor** effectively balanced the **bias-variance trade-off**, making it the strongest predictive model in this task.

---

## 📦 Requirements
