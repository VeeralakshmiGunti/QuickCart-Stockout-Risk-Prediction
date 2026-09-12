# QuickCart Stockout Risk Prediction

Machine Learning-based stockout risk prediction and inventory analysis for QuickCart.

## Project Overview

This project predicts the daily stockout risk of QuickCart inventory using machine learning.

The stockout risk is classified into three categories:

- Safe
- At-Risk
- Imminent

The project helps identify high-risk inventory items early and supports timely replenishment decisions.

## Dataset

The dataset contains daily inventory records for QuickCart stores and products.

- 21,600 inventory records
- 12 stores
- 60 SKUs
- 30 days of daily inventory data
- Date range: October 1–30, 2026

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Data Preparation

The data was cleaned and combined from multiple tables including stores, SKUs, suppliers, events, and daily inventory data.

The following preprocessing steps were performed:

- Checked missing values
- Checked duplicate records
- Standardized city names
- Handled missing supplier reliability values
- Converted date columns
- Merged all required datasets

## Feature Engineering

The following features were created for machine learning:

- Reorder Gap
- Days of Cover Ratio
- Supplier Reliability
- Day of Month
- Days Since Festival Start
- Festival Week
- Product Category

## Machine Learning Models

Two classification models were used:

- Logistic Regression
- Random Forest

## Model Results

| Model | Accuracy | Imminent Recall |
|---|---:|---:|
| Logistic Regression | 85.10% | 71% |
| Random Forest | 92.36% | 78% |

Random Forest performed better than Logistic Regression based on both accuracy and Imminent class recall.

## Key Findings

- The Imminent stockout risk was higher during the festival period.
- Bakery had the highest Imminent stockout risk among the product categories.
- Lower supplier reliability was associated with higher Imminent stockout risk.
- Days of Cover Ratio was the most important feature in the Random Forest model.
- Reorder Gap was the second most important feature.
- Supplier Reliability also contributed to stockout risk prediction.

## Project Visualizations

### Stockout Risk Distribution

![Stockout Risk Distribution](outputs/stockout_risk_distribution.png)

### Festival vs Non-Festival Stockout Risk

![Festival vs Non-Festival Risk](outputs/festival_vs_nonfestival.png)

### Imminent Stockout Risk by Category

![Imminent Risk by Category](outputs/imminent_risk_by_category.png)

### Random Forest Feature Importance

![Random Forest Feature Importance](outputs/random_forest_feature_importance.png)

## Conclusion

This project developed a machine learning approach to predict daily stockout risk for QuickCart inventory.

The data was cleaned, integrated, and analyzed to identify important factors affecting stockout risk. Features such as days of cover ratio, reorder gap, supplier reliability, and festival timing were used for prediction.

Among the two models, Random Forest performed better with 92.36% accuracy and 78% recall for the Imminent class.

The results show that machine learning can help QuickCart identify high-risk inventory items early and support timely replenishment decisions.
