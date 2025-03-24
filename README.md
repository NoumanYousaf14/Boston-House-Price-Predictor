# Boston-House-Price-Predictor


## 📌 Project Overview
This project is a **machine learning model** built to predict house prices in **Boston** using various housing-related features. The model utilizes **RandomForestRegressor** to analyze historical housing data and estimate property values.

## 📊 Dataset
The dataset contains **506 rows** and **14 columns**, including features such as:
- **CRIM**: Per capita crime rate.
- **ZN**: Proportion of residential land zoned for large lots.
- **INDUS**: Proportion of non-retail business acres.
- **CHAS**: Proximity to the Charles River.
- **NOX**: Nitrogen oxide concentration.
- **RM**: Average number of rooms per dwelling.
- **AGE**: Proportion of owner-occupied units built before 1940.
- **DIS**: Weighted distance to employment centers.
- **RAD**: Accessibility to radial highways.
- **TAX**: Property tax rate per $10,000.
- **PTRATIO**: Pupil-teacher ratio in schools.
- **B**: Proportion of the population identifying as Black.
- **LSTAT**: Percentage of lower status population.
- **Price**: Median home price (target variable).

## 🚀 Installation & Setup
To run this project, follow these steps:
```sh
# Clone the repository
git clone https://github.com/NoumanYousaf14/Boston-House-Price-Predictor.git

# Navigate to the project directory
cd Boston-House-Price-Predictor

# Required Dependencies
# Install the following Python libraries before running the project:
pip install scikit-learn pandas numpy matplotlib seaborn jupyter
```

## 🛠 Model Training & Evaluation
The model is trained using **RandomForestRegressor**:
```python
from sklearn.ensemble import RandomForestRegressor
rf = RandomForestRegressor()
rf.fit(X_train, y_train)
y_pred_rf = rf.predict(X_test)
```

### **Feature Importance**
After training, feature importance is extracted using:
```python
importance = rf.feature_importances_
importance_df = pd.DataFrame({'Feature': feature_names, 'Importance': importance})
importance_df.sort_values(by='Importance', ascending=False)
```

### **Performance Metrics**
- **R² Score (CV Score):** Measures how well the model predicts unseen data.
- **Mean Squared Error (MSE):** Evaluates prediction error.
- **Root Mean Squared Error (RMSE):** Measures model accuracy in price units.

## 📉 Results & Insights
- **Most Important Features:** RM, LSTAT, and PTRATIO significantly influence house prices.
- **Model Performance:** Achieved an **R² score of ~85%**, indicating strong predictive power.

## 💡 Future Improvements
- Experiment with **Hyperparameter Tuning**.
- Implement **Feature Engineering** for better insights.
- Try **Deep Learning Models** for higher accuracy.

## 🤝 Contributing
Pull requests are welcome! Feel free to contribute by improving the model or adding new features.

## 📜 License
This project is licensed under the **MIT License**.


