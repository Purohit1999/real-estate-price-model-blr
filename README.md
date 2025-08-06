# 🏡 Bengaluru House Price Prediction

This project is a machine learning solution designed to **predict housing prices in Bengaluru** based on various property features such as location, area type, number of bathrooms, square footage, and more.

The project uses a **Random Forest Regression model** and explores extensive **data preprocessing, feature engineering, model evaluation**, and **visualization** techniques.

---

## 📁 Dataset

- File: `Bengaluru_House_Data.csv`
- Source: Kaggle (or local)
- Features: `location`, `total_sqft`, `bath`, `balcony`, `size`, `area_type`, `availability`, `society`, `price`, etc.

---

## 🧠 Technologies Used

- Python 🐍
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- Pickle (model serialization)

---

## 📌 Project Workflow

### 1. Data Preprocessing
- Removed missing values in key features (`location`, `total_sqft`, etc.)
- Handled `total_sqft` ranges by converting to average
- Extracted BHK from `size` column
- Filled missing values in `balcony`, `availability`, and `society`
- One-hot encoded categorical variables

### 2. Feature Engineering
- Created new feature: `price_per_sqft`
- Removed extreme outliers (1st–99th percentile) from `price_per_sqft`

### 3. Model Training
- Split data into training and test sets (80/20)
- Trained **RandomForestRegressor** with:
  - `n_estimators=100`
  - `max_depth=20`
- Saved the model using `pickle`

### 4. Evaluation Metrics
- **R² Score**
- **Mean Absolute Error (MAE)**
- **Root Mean Squared Error (RMSE)**
- **5-Fold Cross-Validated R² Score**

### 5. Visualization
- Plotted top 20 feature importances
- Visualized the distribution of `price_per_sqft`

---

## 📈 Model Results

| Metric                   | Value        |
|--------------------------|--------------|
| R² Score                 | ~0.64        |
| Mean Absolute Error      | ~50.00       |
| Root Mean Squared Error  | ~75.00       |
| Cross-Validated R² Score | ~0.61        |

> *Note: Values will vary slightly depending on data cleaning and hyperparameters.*

---

## 📦 Output

- Trained model saved as: `bengaluru_price_model_enhanced.pkl`

---

## 📊 Visualizations Included

- Feature importance bar chart (top 20)
- Price per square foot distribution histogram

---

## ✅ Future Enhancements

- Implement hyperparameter tuning using `GridSearchCV`
- Try alternative models: XGBoost, Lasso, etc.
- Add interactive dashboard using Streamlit

---

## 🔗 Author

**Param Purohit**  
GitHub: [@Purohit1999](https://github.com/Purohit1999)

---

