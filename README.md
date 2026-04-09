# 🚗 Car Price Prediction using Machine Learning

## 📌 Project Overview
This project focuses on predicting car prices using machine learning techniques. It involves data cleaning, exploratory data analysis (EDA), feature engineering, and building regression models to estimate vehicle prices based on various attributes.

The dataset contains **370,000+ car listings**, making it a real-world, large-scale data analysis project.

---

## 🎯 Objectives
- Analyze car dataset and understand key features  
- Clean and preprocess real-world noisy data  
- Perform exploratory data analysis (EDA)  
- Build regression models to predict car prices  
- Evaluate and improve model performance  

---

## 📊 Dataset Description
The dataset includes the following features:

- 🚘 Vehicle Type  
- ⚙️ Gearbox  
- ⛽ Fuel Type  
- 📅 Year of Registration  
- 🔋 Power (PS)  
- 🛣️ Kilometer Driven  
- 🏷️ Brand & Model  
- 💲 Price (Target Variable)  

---

## 🧹 Data Cleaning & Preprocessing
- Removed irrelevant columns (index, name, postalCode)  
- Handled missing values using default categories (`unknown`, `nan`)  
- Converted date columns to datetime format  
- Filtered invalid data:
  - Price > 100 and < 150000  
  - Year between 1900 and 2026  
  - Power between 10 and 1000  

---

## 📈 Exploratory Data Analysis (EDA)

### 🔹 Price Distribution
- Most cars fall in the **low to mid price range**
- Data is **right-skewed** with some high-price outliers  

### 🔹 Year of Registration
- Majority of cars are post-2000 models  

### 🔹 Brand Analysis
- Premium brands have significantly higher average prices  

### 🔹 Fuel Type Insights
- Diesel vehicles tend to be priced higher  
- Electric and hybrid segments are emerging  

---

## ⚙️ Feature Engineering
- Selected key features for modeling  
- Applied **One-Hot Encoding** for categorical variables  
- Created a clean dataset suitable for machine learning  

---

## 🔗 Correlation Analysis
Key relationships observed:
- 📈 Power (PS) → Strong positive impact on price  
- 📉 Kilometer → Negative correlation with price  
- 📅 Newer cars → Higher price  

---

## 🤖 Machine Learning Models

### 🔹 Linear Regression
- Baseline model  
- Performance:
  - MAE ≈ 3060  
  - R² ≈ 0.27  
- Limitation: Cannot capture non-linear relationships  

---

### 🔹 Log Transformation (Improvement)
- Applied `log1p()` to normalize skewed price distribution  
- Used `expm1()` to convert predictions back  

✔ Improved performance:
- R² ≈ 0.67  
- Reduced prediction error  

---

### 🔹 Decision Tree Regressor
- Handles non-linear relationships  
- Improved accuracy compared to linear regression  

---

### 🔹 Random Forest Regressor ⭐ (Best Model)
- Ensemble learning method  
- Highest accuracy among all models  

✔ Performance:
- MAE ≈ 1600  
- R² ≈ 0.74  

---

## 📊 Model Comparison

- | Model             | R² Score | MAE   | Performance |
- | ----------------- | -------- | ----- | ----------- |
- | Linear Regression | 0.27     | 3060  | ❌ Poor      |
- | Linear + Log      | 0.67     | 2667  | ⚠️ Moderate |
- | Decision Tree     | 0.74     | 1634  | ✅ Good      |
- | Random Forest     | ~0.74    | ~1634 | 🚀 Best     |

---

## 📊 Model Evaluation Metrics
- Mean Absolute Error (MAE)  
- Mean Squared Error (MSE)  
- R² Score  

---

## 📉 Visualization
- Price distribution histogram  
- Year distribution  
- Boxplots (gearbox vs year)  
- Correlation heatmap  
- Actual vs Predicted scatter plots  

---

## 🧠 Key Insights
- Car price is strongly influenced by power and year  
- Mileage reduces vehicle value significantly  
- Premium brands dominate higher price segments  
- Non-linear models perform better than linear models  

---

## 📌 Conclusion
This project demonstrates how machine learning can effectively predict car prices using real-world data. Advanced models like Random Forest significantly outperform linear regression by capturing complex relationships between features.

---

## 🔮 Future Work
- Implement advanced models like XGBoost  
- Perform hyperparameter tuning  
- Deploy as a web app using Streamlit  
- Include additional features such as location and demand  

---

## 🛠️ Tech Stack
- Python 🐍  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  
- Scikit-learn  

---

## 📁 Project Structure
- Car-Price-Prediction/
- │── autos.csv
- │── car_price_model.ipynb
- │── README.md


---

## 👤 Author
**Sheshu Vardhan**  
Aspiring Data Analyst | Excel | Power BI | Python | SQL | Machine Learning  

---

## ⭐ Support
If you found this project useful, consider giving it a ⭐ on GitHub!