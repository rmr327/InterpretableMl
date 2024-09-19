# Interpretable Ml
This repository includes a demo project that models a company's churn rate using three interpretable modeling frameworks: Linear Regression, Logistic Regression, and Generalized Additive Models. The advantages and disadvantages of each model are discussed in relation to the dataset, and the key assumptions for each model have been tested.

## Intial EDA

![image](https://github.com/user-attachments/assets/69df2e55-cb9e-4b7c-b8c8-c87ba142c56e)
![image](https://github.com/user-attachments/assets/84d5e2b8-f682-4c5a-916e-a877fdc90749)
and so on.. 

![image](https://github.com/user-attachments/assets/c34bb6b4-5e88-461d-b149-bf19c7f0eae7)

![image](https://github.com/user-attachments/assets/c8752294-14fb-4c18-94ea-b90401d4f45b)

## Linear Regression Coeficient importance (Model interpretation in percentage chance of churn)

![image](https://github.com/user-attachments/assets/fba1f482-f02a-4b1b-bde2-f7762d3e823e)

## Logistic Regression Coeficient importance (Model interpretation in Log Odds of churn)

![image](https://github.com/user-attachments/assets/03c92841-9bbc-4c0c-a8cf-9f2c8af2ba54)

## Generalized Additive Model Interpretation (Log Odds of churn in Partial Dependance Plot)

![image](https://github.com/user-attachments/assets/9739104b-63fe-4cdd-a762-a7beb9b02a4e)

and so on..

## Conclusion

In terms of raw performance on the held-out test set, Generalized Additive Models (GAMs) slightly outperform Logistic Regression, which in turn performs marginally better than Linear Regression. Regarding interpretability, Linear Regression is the most straightforward, allowing us to directly interpret the coefficients as changes in the probability of churn. Next is Logistic Regression, which remains quite interpretable but requires us to understand coefficients as changes in the log odds of churn. GAMs are also interpretable, but their interpretation relies on partial dependence plots, which typically demand more time and effort.

When examining key assumptions, Linear Regression fails to meet several, while both Logistic Regression and GAMs pass. The primary strength of Linear Regression is its unparalleled interpretability, though its main weakness is its unsuitability for binary target variables. Logistic Regression effectively extends Linear Regression to binary outcomes, but it sacrifices some interpretability by transitioning from real-world effects to log odds. GAMs excel at modeling non-linear relationships between the target and features, but they rank lowest in interpretability among the three, though they still maintain good interpretability.

For the current analysis, the company should utilize the Logistic Regression model to address their churn rate. This recommendation stems from the invalidation of the Linear Regression model due to numerous assumption violations and the limited performance improvement of the GAM model relative to its interpretability trade-off.
