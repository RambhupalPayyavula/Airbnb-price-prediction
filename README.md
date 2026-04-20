# 🏠 Airbnb Price Prediction — London (ML & Geo-Spatial Analysis)

This project focuses on predicting Airbnb listing prices in London using **data engineering, geographic clustering, and machine learning**. It demonstrates how location, property features, and host activity influence pricing in short-term rental markets.

---

## 📊 Problem Statement

Airbnb pricing is influenced by multiple factors such as:
- Location (latitude, longitude)
- Property characteristics
- Host activity and availability

The goal of this project is to:
- Identify key drivers of Airbnb pricing  
- Cluster listings based on geographic patterns  
- Build models to predict price categories and continuous prices  

---

## ⚙️ Tech Stack

**Language:** Python  
**Data Processing:** pandas, numpy  
**Visualization:** matplotlib, seaborn, plotly  
**Machine Learning:** scikit-learn  

---

## 🧼 Data Pipeline & Engineering

### 🔹 Data Cleaning
- Handled missing values:
  - Categorical → Mode imputation  
  - Numerical → Median imputation  

### 🔹 Outlier Detection
- Applied **Interquartile Range (IQR)** method  
- Removed extreme values to improve model stability  

### 🔹 Feature Engineering
- Created `price_range` categories:
  - Economic, Low-Mid, High-Mid, High  
- Encoded categorical variables using **Label Encoding**  

---

## 🌍 Geographic Clustering

- Applied **Gaussian Mixture Models (GMM)** on:
  - Latitude  
  - Longitude  

- Identified **4 geographic clusters**
- Optimized clustering using **Silhouette Score**

👉 Captured location-based pricing behavior across London neighborhoods  

---

## 🧠 Machine Learning Models

### 1. K-Nearest Neighbors (KNN)
- Tuned `n_neighbors` for optimal classification accuracy  
- Used for **price range classification**

---

### 2. Random Forest Classifier
- Predicted price categories  
- Used for **feature importance analysis**

---

### 3. Random Forest Regressor
- Predicted continuous price values  
- Captured non-linear relationships in data  

---

## 🏆 Key Insights

- **Top Predictors of Price:**
  - `availability_365`
  - `calculated_host_listings_count`
  - `reviews_per_month`

- **Geographic Impact:**
  - High-price clusters concentrated in:
    - Westminster  
    - Kensington  

👉 Location + host activity strongly influence pricing  

---

## 📉 Model Performance

- Evaluated using classification accuracy and regression metrics  
- Compared multiple models to ensure robustness  

---

## 📂 Repository Structure

```bash
Airbnb-Price-Prediction-London/
├── FinalProjectcode.ipynb          # Data cleaning, EDA, modeling
├── FinalprojectPresentation.pptx   # Project summary
├── Airbnb_analysis.docx            # Detailed documentation
