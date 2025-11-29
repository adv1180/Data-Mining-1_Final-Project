# STA 5703 Data Mining Methodology I

## Project: Predicting Asteroid Threat Levels Using Machine Learning

## Project Overview
* **Goal:** Develop supervised and unsupervised machine learning models to predict asteroid threat levels and continuous risk scores using pre-encounter orbital and kinematic features.
* **Dataset:** 89,227 near-Earth object (NEO) close-approach records with features such as miss distance, relative velocity, absolute magnitude, time-to-approach, and threat labels.
* **Data Source:** NASA/JPL Small-Body Database (2024).
* **Tasks:**
  * **Classification:** Predicting categorical threat levels (SAFE, MONITOR, CONCERN, OH\_NO)
  * **Regression:** Modeling the continuous `risk_score`
  * **Unsupervised Learning:** Identifying dynamical groupings in orbital space using PCA and KMeans
* **Validation Strategy:** Time-aware train/test split (train ≤ 2090, test > 2090) and grouped cross-validation based on encounter year to prevent temporal leakage.

---

## Models Implemented
### **Supervised Learning**
* **Linear Regression** (baseline)
* **Ridge Regression** (L2 regularization)
* **Lasso Regression** (L1 regularization)
* **Polynomial Regression** (Degree 2)
* **Spline Regression**
* **Multinomial Logistic Regression** (class-weighted)

### **Unsupervised Learning**
* **Principal Component Analysis (PCA)**
* **KMeans Clustering (k = 5)**
