# House-Price-Prediction
---

# 🏠 House Price Prediction

This project involves building a machine learning model to predict house prices based on various features such as location, size (BHK), square footage, and more. It includes data preprocessing, outlier removal, feature engineering, and model training using linear regression.

---

## 📁 Files

* `House_price_prediction.ipynb` – Jupyter notebook containing the full data analysis and model-building workflow.

---

## 🛠️ Tools & Libraries Used

* Python
* Pandas
* NumPy
* Matplotlib / Seaborn (for visualization)
* Scikit-learn (for model training and evaluation)
* Jupyter Notebook

---

## 📊 Dataset

* The dataset contains information about housing prices including:

  * Area type
  * Availability
  * Location
  * Size (BHK)
  * Total square footage
  * Bath count
  * Price (in lakhs)

---

## ✅ Workflow Summary

1. **Data Loading**

   * Load CSV data using pandas.

2. **Data Cleaning**

   * Remove unnecessary columns (`area_type`, `availability`, `society`).
   * Handle missing values.

3. **Feature Engineering**

   * Extract BHK from the size column.
   * Convert `total_sqft` to numeric.
   * Create a new column for `price_per_sqft`.

4. **Handling Categorical Data**

   * Reduce high-cardinality locations.
   * Use one-hot encoding.

5. **Outlier Removal**

   * Remove outliers based on price per sqft and BHK-to-sqft relationships.
   * Remove unusual bathroom counts.

6. **Model Building**

   * Use `LinearRegression` from Scikit-learn.
   * Split data into training and test sets.
   * Use `GridSearchCV` with `LinearRegression`, `Lasso`, and `DecisionTreeRegressor` for comparison.

7. **Prediction Function**

   * Create a function `predict_price(location, sqft, bath, bhk)` for making predictions.

---

## 🧠 How to Use

You can use the `predict_price()` function at the end of the notebook to make price predictions:

```python
predict_price('1st Phase JP Nagar', 1000, 2, 2)
```

Returns predicted price for a 1000 sqft 2 BHK, 2 Bath apartment in "1st Phase JP Nagar".

---

## 📈 Sample Output

```
Predicted price: ₹ 75.34 Lakhs
```

---

## 🚀 Future Work

* Improve accuracy with more features (e.g., year built, floor, amenities).
* Use advanced ML models like XGBoost, RandomForest.
* Deploy the model using Flask or Streamlit.

---

## 🧑‍💻 Author

* Dibyajyoti Dutta

---
