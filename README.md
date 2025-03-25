#  Car Price Prediction using Machine Learning

##  Overview
This project predicts the selling price of used cars based on various factors such as mileage, fuel type, seller type, transmission, and ownership. The dataset undergoes preprocessing, feature engineering, and model training using multiple machine learning techniques.

##  Features
- **Data Preprocessing**: Handles missing values, removes outliers, and applies transformations.
- **Feature Engineering**: Adds a new feature `car_age` and applies logarithmic transformation.
- **Multiple ML Models**:
  - Linear Regression
  - Lasso Regression
  - Random Forest
  - XGBoost
- **Performance Evaluation**: Uses R² Score, RMSE, and MAE.
- **SHAP Analysis**: Feature importance visualization.
- **Streamlit Web App**: Interactive UI for users to predict car prices.

##  Dataset
The dataset contains the following columns:
- `year`: Manufacturing year of the car (converted to `car_age`).
- `selling_price`: Price of the car (target variable).
- `km_driven`: Kilometers driven.
- `fuel`: Fuel type (Petrol/Diesel/CNG/Electric).
- `seller_type`: Individual or dealer.
- `transmission`: Automatic or manual.
- `owner`: Number of previous owners.

##  Installation & Setup
```bash
# Clone the repository
git clone https://github.com/your-repo/car-price-prediction.git
cd car-price-prediction

# Install dependencies
pip install -r requirements.txt
```

##  Running the Project
1. **Run the machine learning model:**
```bash
python model.py
```
2. **Start the Streamlit web app:**
```bash
streamlit run app.py
```

##  Model Performance
| Model              | R² Score | RMSE  | MAE  |
|-------------------|---------|-------|------|
| Linear Regression | 0.670   | 0.481 | 0.362|
| Lasso Regression  | 0.487   | 0.600 | 0.436|
| Random Forest     | 0.705   | 0.455 | 0.324|
| XGBoost          | 0.724   | 0.440 | 0.320|


## 🖥️ Usage
1. Enter **car details** in the web app (km driven, fuel type, etc.).
2. Click **Predict Price**.
3. View the **predicted selling price**.


##  Feature Importance (SHAP)
SHAP analysis was conducted to understand the most influential factors in predicting car prices.
```python
explainer = shap.Explainer(rf_model, X_train_transformed)
shap_values = explainer(X_train_transformed)
shap.summary_plot(shap_values, X_train_transformed)
```

##  Web App UI Preview
*Include a screenshot of your Streamlit UI here.*

##  Future Enhancements
- Improve model performance with **hyperparameter tuning**.
- Add more **features like car brand, city, and insurance**.
- Deploy the model using **AWS/GCP for online access**.

##  Contribution
Feel free to fork this repository and submit a pull request. Contributions are welcome! 

##  License
This project is licensed under the MIT License.

---
 **Developed with Python**
