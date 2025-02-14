# Predicting Credit Card Debt Balance Using Linear Regression

## Project Overview

This project aims to predict the balance of credit card debt based on various customer features using a linear regression model. The dataset contains information related to customer income, credit card limit, credit rating, age, education, and other relevant features.

## Dataset Description

The dataset used for this project contains the following columns:

| Column     | Description                                       |
|------------|---------------------------------------------------|
| Income     | Income in thousands of dollars                    |
| Limit      | Credit limit                                      |
| Rating     | Credit rating                                     |
| Cards      | Number of credit cards                            |
| Age        | Age of the customer                               |
| Education  | Years of education                                |
| Own        | House ownership (categorical)                     |
| Student    | Student status (categorical)                      |
| Married    | Marital status (categorical)                      |
| Region     | Geographical region (East, West, or South)        |
| Balance    | Average credit card debt for the individual (target variable) |

## Problem Statement

The task is to predict the `Balance` (credit card debt) based on the following features:
- `Income`
- `Limit`
- `Rating`
- `Cards`
- `Age`
- `Education`

## Exploratory Data Analysis

### Univariate Analysis for `Balance`
We performed a histogram plot and KDE (Kernel Density Estimate) to examine the distribution of the target variable, `Balance`. This helped us identify the skewness of the data and any possible outliers.

### Correlation Analysis
We examined the correlation between independent variables to check for potential multicollinearity. We found that `Limit` and `Rating` were highly correlated with `Income`, indicating multicollinearity issues.

### Feature Coefficients
The coefficients obtained from the linear regression model provide insights into the influence of each feature on the predicted balance. The most influential feature is `Limit`, with a coefficient of 473.95.

| Feature    | Coefficient |
|------------|-------------|
| Income     | -266.63     |
| Limit      | 473.95      |
| Rating     | 156.47      |
| Cards      | 26.53       |
| Age        | -10.16      |
| Education  | -3.43       |
| Own        | -6.24       |
| Student    | 121.90      |
| Married    | -2.89       |
| Region     | 4.73        |

### Model Evaluation
- **Mean Squared Error (MSE)**: 7938.24
- **Coefficient of Determination (R-squared)**: 0.9525

The model has a high R-squared value, suggesting a strong fit to the data.

## Residual Analysis

- **Multicollinearity**: We observed that features like `Limit` and `Rating` are highly correlated with `Income`, which could inflate standard errors and make some variables appear statistically insignificant.
  
- **Homoscedasticity**: There is no homoscedasticity, as evidenced by the residual plot. This indicates that the spread of residuals is not constant across all values of the independent variables, which could lead to inefficient estimates and biased standard errors.

- **Shapiro-Wilk Test for Normality**: The data does not follow a normal distribution, with a p-value of 0.0207, leading us to reject the null hypothesis. This suggests that the residuals are not normally distributed.

## Model Implications

- **High MSE**: The model's Mean Squared Error is relatively high, indicating some degree of error in the model predictions. However, the model still performs well in explaining the variance in the data, as seen from the high R-squared value.
  
- **Multicollinearity**: Presence of multicollinearity suggests the need to address this issue through techniques like variance inflation factor (VIF) analysis or feature selection.

- **Residual Distribution**: Non-normal residuals indicate potential issues with the model's assumptions, leading to possible errors in inference and bias in predictions.

- **Overfitting and Underfitting**: The model shows a balance between overfitting and underfitting, as the MSE for both training and test data stabilizes, indicating a well-regularized model.

## Conclusion

This model demonstrates good predictive power with a high R-squared value, but it is important to address the identified issues such as multicollinearity, non-normal residuals, and potential heteroscedasticity for further improvements. Addressing these could enhance the robustness and accuracy of the predictions.

## 🌍 Explore More Projects  
For more exciting machine learning and AI projects, visit **[The iVision](https://theivision.wordpress.com/)** and stay updated with the latest innovations and research! 🚀  

---
