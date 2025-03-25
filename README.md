#  Car Price Prediction

##  Overview
This project predicts the **selling price of used cars** based on various features such as mileage, fuel type, car age, and more. The model is trained using machine learning algorithms and deployed as a **Streamlit web app**.

##  Features
- **Data Preprocessing**: Feature engineering, outlier removal, encoding, and scaling.
- **Machine Learning Models**:
  - Linear Regression
  - Lasso Regression
  - Random Forest Regressor
  - XGBoost Regressor
- **Feature Importance Analysis**: SHAP (SHapley Additive exPlanations) to understand model decisions.
- **Web App Deployment**: Streamlit-based UI for price prediction.

##  Dataset
The dataset includes used car details like:
- `selling_price`: Target variable (log-transformed for normalization).
- `year`: Manufacturing year (converted to `car_age`).
- `km_driven`: Distance traveled (log-transformed).
- `fuel`, `seller_type`, `transmission`, `owner`: Categorical variables.

##  Model Performance
| Model | R² Score |
|--------|--------|
| Linear Regression | 0.694 |
| Lasso Regression | 0.487 |
| Random Forest | **0.705** |
| XGBoost | **0.724** |

##  Installation & Setup
1. **Clone the repository**
   ```bash
   git clone https://github.com/your-repo/car-price-prediction.git
   cd car-price-prediction
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Streamlit App**
   ```bash
   streamlit run app.py
   ```

##  Usage
1. Enter **car details** in the web app (km driven, fuel type, etc.).
2. Click **Predict Price**.
3. View the **predicted selling price**.

##  SHAP Feature Importance
SHAP analysis reveals the most influential factors in price prediction:
- `km_driven` and `car_age` significantly impact price.
- **Fuel type** and **transmission** also play a role.

##  Future Improvements
- **Hyperparameter tuning** for better accuracy.
- **Deployment on cloud platforms** (Streamlit Cloud, Render).
- **Better UI with interactive graphs**.

##  Contributing
Feel free to open issues or submit pull requests!

##  License
This project is licensed under the **MIT License**.

---
Made by Shalu Yadav

