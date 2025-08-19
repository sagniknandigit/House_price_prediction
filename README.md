🏡 House Price Prediction with Linear Regression

💡 Project Overview

This project demonstrates a simple yet effective approach to predicting house prices using Linear Regression. We use a synthetic dataset that simulates various housing features to build and evaluate a predictive model. The goal is to understand the fundamental steps involved in a machine learning regression task, from data preparation to model evaluation and visualization.

✨ Features

The dataset used in this project includes the following features:

Area_sqft: The size of the house in square feet.

Bedrooms: Number of bedrooms in the house.

Bathrooms: Number of bathrooms in the house.

YearBuilt: The year the house was constructed.

Location: Categorical feature indicating the area (e.g., 'Downtown', 'Suburban', 'Rural', 'Urban outskirts').

Price_USD: The target variable – the price of the house in USD.

🛠️ Tools and Libraries Used

Python 3.x: The core programming language.

Pandas: For data manipulation and analysis.

NumPy: For numerical operations, especially array handling.

Scikit-learn: The primary machine learning library for model building, preprocessing, and evaluation.

LinearRegression

train_test_split

OneHotEncoder

ColumnTransformer

Pipeline

Matplotlib: For creating static, interactive, and animated visualizations.

Seaborn: For creating aesthetically pleasing statistical graphics, built on Matplotlib.

🚀 Methodology

The project follows a standard machine learning workflow:

1. Dataset Generation
   
A synthetic dataset of 1000 house entries is generated to simulate real-world housing data, including various features and a calculated price with added noise. This ensures reproducibility and self-containment of the project.

2. Data Preprocessing
   
Feature-Target Split: The dataset is divided into features (X) and the target variable (y).

Categorical Encoding: The Location (categorical) feature is converted into a numerical format using OneHotEncoder. This creates new binary columns for each unique location.

ColumnTransformer: Used to apply the OneHotEncoder only to the Location column, while numerical columns are passed through unchanged.

Train-Test Split: The data is split into 80% for training the model and 20% for testing its performance on unseen data (test_size=0.2, random_state=42).

3. Model Training
   
Linear Regression: A simple yet powerful supervised learning algorithm for predicting a continuous target variable.

Pipeline: A Pipeline is used to streamline the workflow, combining the preprocessing steps (ColumnTransformer) and the LinearRegression model into a single object. This ensures consistency when training and making new predictions.

The model is trained (fit) on the X_train and y_train datasets.

4. Model Evaluation
   
The trained model makes predictions on the X_test (unseen) data.

R-squared (R2) Score: The primary metric used to evaluate the model's performance. It measures the proportion of the variance in the dependent variable that can be predicted from the independent variables. A score closer to 1 indicates a better fit.

5. Prediction on Unknown Data
   
The trained model_pipeline can then be used to predict the price of a hypothetical "unknown" house by providing its features in the correct format.

📊 Results and Visualizations

After training, our model achieved a high R-squared score, indicating its strong predictive capability on the synthetic data.

R-squared Score on Test Set: <YOUR_R2_SCORE_HERE> (e.g., 0.95)

Predicted Price for an Example Unknown House: <YOUR_PREDICTED_PRICE_HERE> (e.g., $345,678.90)

Actual vs. Predicted Prices

This scatter plot illustrates how closely the model's predictions align with the actual house prices in the test set. Points closer to the red dashed line (where actual = predicted) indicate better predictions.

Description: A scatter plot with 'Actual Prices (USD)' on the X-axis and 'Predicted Prices (USD)' on the Y-axis. A red dashed line representing ideal predictions (y=x) passes through the plot. Most data points should cluster closely around this line.

Residual Plot

The residual plot helps in diagnosing the model's performance. Residuals (Actual - Predicted) should be randomly scattered around zero, with no discernible patterns. Any pattern might suggest that the model is missing some underlying relationship in the data.

Description: A scatter plot with 'Predicted Prices (USD)' on the X-axis and 'Residuals (Actual - Predicted)' on the Y-axis. A horizontal red dashed line at Y=0 is included. Data points should appear randomly scattered above and below the zero line, without any clear shape or trend.

🏃 How to Run the Code

To run this project on your local machine:

Clone the repository (if applicable) or copy the code:

# If you have a GitHub repository

git clone <repository-url>
cd <project-directory>

If you just copied the code, save it as a .py file (e.g., house_price_predictor.py).

Install the necessary libraries:

pip install pandas numpy scikit-learn matplotlib seaborn

Run the Python script:

python house_price_predictor.py

The script will print the data preview, training progress, model performance, a sample prediction, and then display two plots (Actual vs. Predicted, and Residuals).

Enjoy exploring the world of Machine Learning! 🚀
