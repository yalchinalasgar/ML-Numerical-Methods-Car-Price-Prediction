# 🚗 Rusty Bargain Used Car Sales 

## 📌 Task Description:

Rusty Bargain is developing an app to attract new customers, and they need to be able to quickly find out the market value of a car. 
We are given access to historical data: technical specifications, trim, and prices. 
Rusty Bargain wants a model that will predict the value of the car, while also considering the quality and speed of the prediction, and also the time required for training.

---

## 📊 Dataset

* Source: 'https://code.s3.yandex.net/datasets/car_data.csv'
* Records: ~355,000 samples

### Feature Columns:
    
DateCrawled — date the profile was downloaded from the database  
VehicleType — vehicle body type  
RegistrationYear — vehicle registration year  
Gearbox — gearbox type  
Power — engine power (hp)  
Model — vehicle model  
Mileage — vehicle mileage (km)  
RegistrationMonth — vehicle registration month  
FuelType — fuel type  
Brand — vehicle brand  
NotRepaired — whether the vehicle has been repaired or not  
DateCreated — date when the profile was created  
NumberOfPictures — number of vehicle pictures  
PostalCode — postal code of the profile owner  
LastSeen — date of the user's last activity

### Target Variable:

Price — vehicle price (Euro)


---

## ⚙️ Project Workflow

1. Introduction
2. Data Loading
3. Data Cleaning
4. Exploratory Data Analysis
5. Feature Engineering
6. Model Training
7. Model Evaluation
8. Sanity Check
9. Conclusion
10.Summary

---

## 🤖 Models Used

* Linear Regression (Baseline Model)
* Decision Tree
* Random Forest
* XGBoost
* LightGBM
* CatBoost

📌 Boosting models (XGBoost, LightGBM, CatBoost) showed very similar performance and can be used as strong alternatives to each other.

---

## 📉 Evaluation Metric

* RMSE (Root Mean Squared Error)

The target variable (Price) was log-transformed using `log1p()` to reduce skewness and improve model performance.

For interpretability, predictions were converted back to the original price scale using `expm1()`, and RMSE is reported in **Euros (€)**.

Lower RMSE indicates better model performance.

---

## 🏆 Results

| Model             |   RMSE  |
| ----------------- | ------- |
| Linear Regression | 2409.05 |
| Decision Tree     | 1603.44 |
| Random Forest     | 1690.06 |
| XGBoost           | 1401.87 |
| LightGBM          | 1461.61 |
| CatBoost          | 1438.58 |

✅ Best Model: **XGBoost (Lowest RMSE & Fast Prediction)**

---

## 📊 Visualizations

* Price Distribution
* Box Plots for Outlier Detection
* Feature Importance
* Bar Chart for Models Results

---

## 🚀 How to Run

```bash
# Clone repository
git clone https://github.com/yalchinalasgar/ML-Numerical-Methods-Car-Price-Prediction

# Navigate to project folder
cd ML-Numerical-Methods-Car-Price-Prediction

# Install dependencies
pip install -r requirements.txt

# Run notebook
jupyter notebook
```

---

## 🧠 Key Insights

* Car age and mileage are the most important factors affecting price
* Newer cars tend to have significantly higher prices
* Brand plays a crucial role in price prediction
* Boosting models outperform traditional regression models

---

## 📌 Future Improvements

* Hyperparameter tuning
* Model deployment (Streamlit / Flask)
* Add more real-world data
* Try deep learning models

---

## 📬 Contact

If you have any questions or suggestions, feel free to reach out!
