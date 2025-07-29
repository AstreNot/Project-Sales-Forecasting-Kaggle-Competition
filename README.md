# Kaggle Sticker Sales Prediction using XGBoost and Radial Basis Function
In this project, I developed a regression model to predict the number of sticker units sold using historical sales data. The data was sourced from a Kaggle competition-style dataset with separate training and test files. I carried out this project using Python, Pandas, and XGBoost, applying a combination of time-based feature engineering, Fourier transforms, and categorical encoding to build an effective predictive model.

## Problem Statement
The objectives of this project were:
1. Build a machine learning model to predict future sticker sales (num_sold) with high accuracy.
2. Leverage time-based and categorical features to extract seasonality and trends.
3. Improve predictive power by incorporating Fourier-based transformations.
4. Evaluate model performance using appropriate metrics (e.g., RMSE).
5. Generate predictions for a holdout test dataset for potential Kaggle submission.

## Tools & Technologies
Python Libraries:
- pandas, numpy for data manipulation
- matplotlib, seaborn for visualization
- xgboost for model training
- sklearn for preprocessing, data splitting, and evaluation
- sklego for advanced feature engineering (Fourier transform)

## ETL & Feature Engineering
The dataset was divided into training and test sets, with the training data used to build and validate the model.
Data preprocessing steps included:
1. Converting date columns to proper datetime format.
2. Replacing null values with 0.
3. Extracting time-based features.
4. Applying Radial Basis Function to extract seasonal patterns from the day of the month.
5. Encoding categorical features (such as country, store, and product) using one-hot encoding.
6. Combining all features into a final training matrix ready for modeling.

## Model Development
A regression model was trained using the XGBoost algorithm. The dataset was split into training and validation sets to test the model’s generalization performance. The evaluation was done using Root Mean Squared Error (RMSE), a standard metric for regression problems.

The model showed strong predictive performance and captured the influence of both temporal trends and categorical variables. Fourier-transformed features helped capture periodic patterns in the sales data that wouldn't be detected using basic time variables alone.

## Prediction & Submission
After training and validating the model, the same preprocessing steps were applied to the test data. Predictions were generated and structured into a final output format for submission, replicating a standard Kaggle workflow.

## Results
1. The model was able to generalize well with an RMSE score of 0.62.
2. Temporal features, especially with Fourier transformation, improved model performance by capturing hidden patterns in the sales data.
3. One-hot encoding of categorical variables allowed the model to distinguish between product, store, and regional effects on sales.

## Recommendations
1. Future improvements can include hyperparameter tuning, feature selection, or the use of ensemble techniques.
2. Incorporating external data such as holidays, promotions, or regional demographics could further improve model accuracy.

## Conclusion
This project demonstrates the value of proper feature engineering and model selection in predictive analytics. XGBoost, combined with thoughtful preprocessing, provides a powerful approach for forecasting time-sensitive metrics like sales.

It also reinforces the importance of understanding the nature of time series data and how techniques like Fourier transformation can extract meaningful seasonal trends that would otherwise remain hidden.
