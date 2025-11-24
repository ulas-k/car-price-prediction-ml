# car-price-prediction-ml
Car price prediction using ML. Includes EDA, preprocessing (OHE + scaling), sklearn Pipeline, Linear Regression model, and performance metrics.

🚗 Car Price Prediction – Machine Learning Project

This project aims to build an end-to-end machine learning model that predicts car prices based on various technical and categorical features. 

The workflow includes data cleaning, exploratory data analysis (EDA), feature engineering, preprocessing with ColumnTransformer, and regression modeling using a complete sklearn Pipeline.

📌 Project Goal

The main objective is to estimate the price of a car using its structural and performance characteristics.

To achieve this, the following steps were performed:

Loaded and explored the dataset

Cleaned and prepared the data

Performed visual EDA

Engineered new features (brand extraction & typo correction)

Encoded categorical variables

Scaled numerical features

Built a regression model

Evaluated performance using MAE and R² metrics

📂 Dataset

carprice.csv includes features such as:

Car dimensions

Engine size

Horsepower

City & highway MPG

Drive wheel / engine location

Fuel type

Body style

Number of doors

carCompany (engineered from CarName)

🎯 Target variable: price

Additional preprocessing:

Extracted manufacturer name from CarName

Fixed spelling inconsistencies (vokswagen → volkswagen, toyouta → toyota, etc.)

Removed redundant columns

🔧 Technologies Used

Python

Pandas

NumPy

Seaborn

Matplotlib

Scikit-Learn

Google Colab

🔍 Exploratory Data Analysis (EDA)

The EDA phase includes:

✔ Histograms for numerical features

To analyze distributions and detect outliers.

✔ Countplots for categorical features

To examine category frequency and imbalance.

✔ Correlation heatmap

To identify relationships between numerical variables and detect strong predictors of price.

🧼 Data Cleaning & Feature Engineering

Extracted carCompany from CarName

Normalized incorrect brand spellings

Dropped unnecessary columns

Identified numerical and categorical column groups

Prepared dataset for modeling

⚙️ Preprocessing Pipeline

A complete preprocessing pipeline was created using ColumnTransformer:

StandardScaler → for numerical features

OneHotEncoder (handle_unknown="ignore") → for categorical features

Combined using an sklearn Pipeline along with the regression model

This ensures a clean, automated, and reproducible ML workflow.

🤖 Modeling

Model used:

➡️ Linear Regression

Train–test split:

80% training

20% testing

random_state=42 (for reproducibility)

📈 Model Performance

MAE: 1806.44

R² Score: 0.9008

These results indicate that the model explains 90% of the variance in car prices and averages $1806 absolute error — a strong performance for a linear model.

🚀 How to Run

Clone the repository:

git clone https://github.com/<your-username>/car-price-prediction-ml

Open car-price-prediction.ipynb

Upload carprice.csv

Run all cells sequentially

⭐ Future Improvements

Add advanced models (Random Forest, XGBoost, LightGBM)

Apply hyperparameter tuning (GridSearchCV)

Compare RMSE between models

Build a simple Streamlit web application

Add SHAP/feature importance analysis

🙌 Feedback

Feedback, suggestions, and contributions are always welcome!
