# Machine Learning Case Study – Viva Questions and Answers

## Project: Estimating Passenger Demand for Transport Services Using Machine Learning

This document contains important and simple viva questions and answers related to the Machine Learning case study.

## 1. Project Introduction

### Q1. What is the title of your project?
**Answer:** Estimating Passenger Demand for Transport Services from Historical and Contextual Data Using Machine Learning.

### Q2. What is the main objective of your project?
**Answer:** The main objective is to predict passenger demand using historical data, time information, and weather conditions.

### Q3. Why did you choose this project?
**Answer:** I chose this project to understand how Machine Learning can help predict transport demand and support

transport planning.

### Q4. Which dataset did you use?
**Answer:** I used the hourly bike-sharing dataset from the UCI Machine Learning Repository.

### Q5. How many observations are present in the original dataset?
**Answer:** The original dataset contains 17,379 hourly observations.

### Q6. What does the dataset represent?
**Answer:** It represents hourly bike-sharing demand in Washington, D.C., during 2011 and 2012.

### Q7. What is the target variable in your project?
**Answer:** The target variable is `cnt`, which represents the total number of bike trips recorded per hour.

### Q8. Is this a classification or regression problem?
**Answer:** It is a regression problem because we predict a numerical value representing passenger demand.

## 2. Machine Learning Basics

### Q9. What is Machine Learning?
**Answer:** Machine Learning is a branch of Artificial Intelligence that enables computers to learn patterns from data and make predictions.

### Q10. What is supervised learning?
**Answer:** Supervised learning is a type of Machine Learning in which a model learns from labelled data containing input features and the expected output.

### Q11. Which type of Machine Learning did you use?
**Answer:** I used supervised learning, specifically regression.

### Q12. Which algorithms did you use in your project?
**Answer:** I used Linear Regression, Decision Tree Regression, and Random Forest Regression.

### Q13. What is Linear Regression?
**Answer:** Linear Regression predicts a numerical value by learning the relationship between input features and the target variable.

### Q14. What is Decision Tree Regression?
**Answer:** Decision Tree Regression predicts numerical values by splitting data into smaller groups based on feature conditions.

### Q15. What is Random Forest Regression?
**Answer:** Random Forest Regression combines multiple decision trees to produce a prediction. It often provides better accuracy and reduces overfitting compared with a single decision tree.

### Q16. Which model performed best in your project?
**Answer:** Random Forest Regression performed best among the evaluated models.

## 3. Data Preprocessing

### Q17. What is data preprocessing?
**Answer:** Data preprocessing is the process of preparing raw data for Machine Learning by cleaning and transforming it.

### Q18. Which features were used in your project?
**Answer:** The features included hour, weather, calendar information, previous-hour demand, rolling averages, and cyclical time features.

### Q19. What is a lag feature?
**Answer:** A lag feature uses a previous observation to help predict the current value. For example, `lag_1h` represents demand from the previous hour.

### Q20. What is a rolling mean?
**Answer:** A rolling mean is the average of values over a specified period. It helps identify recent demand patterns.

### Q21. Why are time-based features important?
**Answer:** Passenger demand can vary by hour, day, and season. Time-based features help the model learn these patterns.

### Q22. What is the purpose of training and testing data?
**Answer:** Training data is used to teach the model, while testing data is used to evaluate its performance on unseen observations.

## 4. Code and Evaluation

### Q23. Which programming language did you use?
**Answer:** I used Python for data processing, model training, and evaluation.

### Q24. Which libraries did you use?
**Answer:** I used Pandas, NumPy, Scikit-learn, and Matplotlib.

### Q25. What is Pandas used for?
**Answer:** Pandas is used to load, process, clean, and analyse structured data.

### Q26. What is NumPy used for?
**Answer:** NumPy is used for numerical calculations and working with arrays.

### Q27. What is Scikit-learn?
**Answer:** Scikit-learn is a Python library that provides Machine Learning algorithms and evaluation tools.

### Q28. What is the purpose of the `fit()` function?
**Answer:** The `fit()` function trains the Machine Learning model using the training data.

### Q29. What is the purpose of the `predict()` function?
**Answer:** The `predict()` function generates predictions using a trained model.

### Q30. What is MAE?
**Answer:** MAE stands for Mean Absolute Error. It measures the average absolute difference between actual and predicted values. A lower MAE indicates better predictions.

### Q31. What is RMSE?
**Answer:** RMSE stands for Root Mean Squared Error. It measures prediction errors while giving greater weight to larger errors. A lower RMSE is generally better.

### Q32. What is the R² score?
**Answer:** R² measures how well a regression model explains the variation in the target variable. A value closer to 1 generally indicates a better fit.

### Q33. What is WAPE?
**Answer:** WAPE stands for Weighted Absolute Percentage Error. It expresses the total absolute prediction error as a percentage of the total actual demand. A lower WAPE is better.

## 5. Results and Conclusion

### Q34. What were the results of your Random Forest model?
**Answer:** The model achieved the following results:

- **MAE:** 34.43
- **RMSE:** 55.49
- **R² Score:** 0.936
- **WAPE:** 13.90%

### Q35. Which feature was the most important?
**Answer:** The most important feature was `lag_1h`, which represents demand during the previous hour.

### Q36. Why is previous-hour demand important?
**Answer:** Demand in the current hour is often related to demand in the previous hour, so historical demand helps the model make better predictions.

### Q37. What are the applications of your project?
**Answer:** The project can help transport planners estimate demand, allocate resources, and improve transport service planning.

### Q38. What are the limitations of your project?
**Answer:** The model may not accurately predict unexpected demand spikes or sudden changes in travel patterns.

### Q39. What is the future scope of your project?
**Answer:** Future improvements could include using more transport datasets, trying advanced Machine Learning algorithms, and regularly retraining the model with updated data.

### Q40. How is data privacy maintained?
**Answer:** The project uses aggregate trip data rather than personal passenger information and avoids using personal identifiers.

### Q41. What is the final conclusion of your project?
**Answer:** The project demonstrates that Machine Learning can estimate hourly mobility demand from historical and contextual data. Random Forest Regression achieved the best performance among the evaluated models.

---

## Quick Revision

| Topic | Important Point |
|---|---|
| Dataset | UCI hourly bike-sharing dataset |
| Original observations | 17,379 |
| Target variable | `cnt` |
| Problem type | Supervised regression |
| Best model | Random Forest Regression |
| Most important feature | `lag_1h` |
| Programming language | Python |
| Main library | Scikit-learn |
| MAE | 34.43 |
| RMSE | 55.49 |
| R² Score | 0.936 |
| WAPE | 13.90% |

**Note:** This dataset represents bike-sharing demand, so it serves as a proxy for transport or mobility demand rather than directly measuring bus or metro passenger demand.

## 3. 10 Rapid-Fire Questions & Answers

### Q1. What is the primary target variable?
**Answer:** `cnt`, representing the total number of bike trips recorded per hour.

### Q2. How many features were engineered in total?
**Answer:** A total of **22 features** were engineered, including time, calendar flags, weather, lag features, and rolling statistics.

### Q3. What is the exact train-test split ratio?
**Answer:** The dataset was split chronologically into **80% training data (13,768 records)** and **20% testing data (3,443 records)**.

### Q4. Why did you use `max_features='sqrt'`?
**Answer:** It allows each tree to consider a random subset of features at each split, helping reduce correlation between trees in the Random Forest.

### Q5. What was your primary model's R² score?
**Answer:** The Random Forest model achieved an **R² score of 0.936**, indicating a strong fit on the test data.

### Q6. What was your primary model's RMSE?
**Answer:** The model achieved an **RMSE of 55.49 trips per hour**.

### Q7. Which feature had the highest feature importance?
**Answer:** `lag_1h`, representing demand from one hour earlier, had the highest reported feature importance at approximately **68.3%**.

### Q8. Why did you avoid random train-test shuffling?
**Answer:** Because the data is time-dependent. A chronological split helps prevent future observations from leaking into the training data when evaluating predictions on later periods.

### Q9. How does your project address privacy under the DPDP Act, 2023?
**Answer:** The project uses aggregated hourly demand counts rather than personal smart-card IDs. This reduces the use of personal information. Legal compliance depends on the full data-processing practices and applicable requirements.

### Q10. Why did you use WAPE instead of MAPE?
**Answer:** MAPE can become extremely large or undefined when actual demand is zero or very low. WAPE calculates total absolute error relative to total actual demand, making it more suitable for evaluating aggregate demand forecasts.

---

**Quick Revision Table**

| Parameter | Value |
|---|---|
| Target variable | `cnt` |
| Engineered features | 22 |
| Training records | 13,768 |
| Testing records | 3,443 |
| Split ratio | 80:20 |
| Best model | Random Forest Regression |
| R² Score | 0.936 |
| RMSE | 55.49 trips/hour |
| Most important feature | `lag_1h` |
| Feature importance | Approximately 68.3% |
| Error metric | WAPE |

**Note:** The feature count, feature importance, and evaluation values above reflect the figures supplied in the case-study notes. Be prepared to explain them using your actual code and results.
