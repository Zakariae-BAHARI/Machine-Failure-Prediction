﻿# Machine-Failure-Prediction

## Project Overview

This project aims to predict machine failures using the AI4I 2020 Predictive Maintenance dataset. By analyzing different features and their correlations with machine failures, we build a Random Forest Classifier to identify potential failures before they occur. The project also includes visualizations to better understand the data and the model's performance.

---

## Dataset

The dataset used in this project is `ai4i2020.csv`, which includes:

- **UDI:** Unique identifier for each data point
- **Product ID:** Identifier for the product
- **Type:** Type of product (L, M)
- **Air temperature [K]:** Air temperature in Kelvin
- **Process temperature [K]:** Process temperature in Kelvin
- **Rotational speed [rpm]:** Rotational speed in RPM
- **Torque [Nm]:** Torque in Newton-meters
- **Tool wear [min]:** Tool wear in minutes
- **Machine failure:** Indicator if a machine failure occurred (1) or not (0)
- **TWF:** Tool wear failure (1) or not (0)
- **HDF:** Heat dissipation failure (1) or not (0)
- **PWF:** Power failure (1) or not (0)
- **OSF:** Overstrain failure (1) or not (0)
- **RNF:** Random failures (1) or not (0)

## Analysis and Modeling

### Correlation Analysis

Calculated the correlation matrix to understand the relationships between features and the target variable ('Machine failure'). Identified important features for prediction:

- Strong correlations: HDF, OSF, PWF
- Moderate correlations: TWF, Torque [Nm], Tool wear [min]
- Weak correlations: Air temperature [K], Rotational speed [rpm], Process temperature [K], Type_L, UDI, Type_M, RNF

### Model Building

- Selected relevant features based on the correlation analysis.
- Split the data into training and testing sets using `train_test_split()`.
- Built a Random Forest Classifier and evaluated its performance using accuracy score, confusion matrix, and classification report.
- Determined feature importance using the trained Random Forest model.

### Visualizations

- Distribution of 'Machine failure' using a count plot.
- Correlation heatmap to visualize relationships between features.
- Feature importance bar chart to show the most influential features.
- Pairplot and PairGrid to explore key features in relation to 'Machine failure'.
- Box plots for key features grouped by 'Machine failure' status.
- Bar plot to show the distribution of different failure modes.

## Results

- The Random Forest Classifier achieved an accuracy of 99.90%.
- Key features influencing machine failures include HDF, OSF, PWF, TWF, and Torque [Nm].
- Visualizations provided insights into data distribution, feature correlations, and model performance.

## Conclusion

The project successfully predicted machine failures using a Random Forest Classifier with high accuracy. Important features were identified, and visualizations helped in understanding the data and model results. This approach can be used for predictive maintenance in real-world scenarios to minimize machine downtime and enhance operational efficiency.
