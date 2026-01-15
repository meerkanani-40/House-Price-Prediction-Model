# House Price Prediction using Machine Learning

## Project Overview
This project implements a machine learning pipeline to predict house prices based on selected numerical features such as area, quality, and number of rooms. The goal of this project is to demonstrate a clear understanding of the end-to-end machine learning workflow, including data analysis, model training, evaluation, and reuse of the trained model for future predictions.

The project is designed to be **simple, interpretable, and explainable**, making it suitable for learning and interview discussions.

## Project Structure
house-price-prediction/<br>
│<br>
├── data/<br>
│ └── train.csv<br>
│<br>
├── model/<br>
│ └── house_price_model.pkl<br>
│<br>
├── train.py<br>
├── predict.py<br>
└── README.md<br>

## Dataset
- **Source:** Kaggle – *House Prices: Advanced Regression Techniques*
- **Format:** CSV
- **Description:** Each row represents a house, and columns represent house attributes and the sale price.

### Selected Features
To keep the model simple and interpretable, the following numerical features were used:
- `LotArea` – Lot size in square feet
- `OverallQual` – Overall material and finish quality
- `YearBuilt` – Construction year
- `TotalBsmtSF` – Basement area
- `GrLivArea` – Above ground living area
- `BedroomAbvGr` – Number of bedrooms above ground

**Target Variable:**
- `SalePrice` – Final sale price of the house

## Exploratory Data Analysis (EDA)
The following EDA steps were performed:
- Inspected dataset shape, columns, and data types
- Analyzed summary statistics to understand feature ranges
- Checked missing values and their proportions
- Visualized the distribution of house prices
- Plotted feature vs target relationships
- Performed correlation analysis to justify feature selection

These steps helped ensure data quality and feature relevance before model training.

## Data Preprocessing
- Selected relevant numerical features
- Handled missing values using **median imputation**
- Separated features (`X`) and target (`y`)
- Split data into training and testing sets (80/20 split)

## Model Training
- **Algorithm Used:** Linear Regression
- **Reason:** Simple, interpretable baseline model for regression problems
- **Library:** scikit-learn

The model was trained using the training dataset and evaluated on unseen test data.

## Model Evaluation
The model was evaluated using:
- **Mean Squared Error (MSE)** – Measures average squared prediction error
- **R² Score** – Measures how well the model explains variance in house prices

An Actual vs Predicted plot was also used to visually inspect model performance.

## Model Saving (Using Pickle)
After training, the model was saved using Python’s built-in `pickle` library. This allows the trained model to be reused later without retraining.

Saved model location:
model/house_price_model.pkl
