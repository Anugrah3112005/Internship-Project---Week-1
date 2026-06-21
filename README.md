 # House Price Prediction

This project predicts residential house prices using machine learning on the Kaggle **Housing Prices Dataset**. It includes data cleaning, exploratory data analysis, regression modeling, visualizations, and a short business-oriented summary of the findings.

## Project Overview

Real estate pricing is often influenced by guesswork or rough comparisons. In this project, I built regression models to estimate house prices based on property features such as:

- area
- bedrooms
- bathrooms
- stories
- parking
- furnishing status
- amenities like air conditioning, basement, guest room, and main road access

The main goal was to identify the features that most strongly affect house prices and compare the performance of two regression models.

## Dataset

- **Source:** Kaggle Housing Prices Dataset
- **Link:** [kaggle.com](https://www.kaggle.com/datasets/yasserh/housing-prices-dataset)
- **File used:** `Housing.csv`

### Dataset summary

- **Rows:** 545
- **Columns:** 13
- **Target variable:** `price`

Features include both numerical and categorical variables such as property size, room counts, parking availability, and furnishing/amenity details.

## Objectives

The project covers the following tasks:

1. Load and explore the dataset
2. Clean and preprocess the data
3. Encode categorical variables
4. Train regression models
5. Evaluate model performance
6. Visualize price distribution and feature relationships
7. Summarize business insights

## Tools and Libraries

- **Python 3**
- **Jupyter Notebook**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **Scikit-learn**

## Workflow

### 1. Data Loading and Exploration

- Loaded the dataset using Pandas
- Displayed sample rows
- Checked dataset shape
- Identified target and feature columns
- Verified missing values

### 2. Data Cleaning and Preprocessing

- Checked for null values
- Removed duplicate rows if present
- Converted categorical columns into numeric format using one-hot encoding
- Prepared the dataset for model training

### 3. Model Building

Two regression models were trained and compared:

- **Linear Regression**
- **Random Forest Regressor**

The dataset was split into training and testing sets using an **80/20** ratio.

## Model Evaluation

The models were evaluated using:

- **MAE** - Mean Absolute Error
- **RMSE** - Root Mean Squared Error
- **R2 Score**

### Results

| Model | MAE | RMSE | R2 Score |
|---|---:|---:|---:|
| Linear Regression | 970,434 | 1,324,507 | 0.653 |
| Random Forest Regressor | 1,021,546 | 1,400,566 | 0.612 |

### Performance Summary

Linear Regression performed slightly better than Random Forest on this dataset, with lower prediction error and a higher R2 score. Both models explained around 60-65% of the variation in house prices.

## Visualizations

This project includes at least three visualizations:

- **Histogram of house prices** to understand the price distribution
- **Correlation heatmap** to identify relationships between features and price
- **Actual vs Predicted scatter plot** to compare model predictions with real values

Saved chart images are included in the `charts/` folder.

## Key Insights

- **Area** had the strongest influence on house price
- **Bathrooms** and **air conditioning** also showed strong positive impact
- Some comfort-related amenities contributed more to pricing than expected
- The models performed reasonably well, but location-specific features could likely improve predictions further

## Business Recommendation

For property investors or real estate businesses, improvements that increase usable area and comfort features, especially **air conditioning**, may provide stronger pricing benefits based on this dataset.

## Repository Structure

```text
HousePricePrediction/
│
├── analysis.ipynb
├── Housing.csv
├── summary.pdf
├── README.md
└── charts/
    ├── price_distribution.png
    ├── correlation_heatmap.png
    └── actual_vs_predicted.png

