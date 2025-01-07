# Board Game Ratings Prediction

This project involves predicting the average ratings of board games based on various numerical features from a dataset of games. The prediction is carried out using machine learning models, specifically Linear Regression (LR) and Random Forest Regressor (RFR). Below is an overview of the process and the steps involved.

## Project Overview

This project aims to:
1. **Load and clean** a dataset of games.
2. **Visualize** the distribution of ratings and correlations among the features.
3. **Split the data** into training and test sets.
4. **Train machine learning models** (Linear Regression and Random Forest Regressor) to predict the average rating of a game.
5. **Evaluate the models** by comparing predictions to actual values and computing the Mean Squared Error (MSE).
6. **Make predictions** on individual rows from the test set to showcase model performance.

## Steps

### 1. Load the Data

The data is loaded from a CSV file `games.csv` using `pandas.read_csv`. After reading the file, we display the column names and the shape of the dataset.

### 2. Data Preprocessing

The dataset is cleaned by:
- Removing rows with zero ratings.
- Removing rows with missing values (NaN).
- Filtering out games without any user reviews.

### 3. Data Visualization

We generate histograms to visualize the distribution of ratings in the `average_rating` column.

We also create heatmaps to visualize correlations between numerical features. This is done by selecting only the numeric columns and calculating their correlation matrix.

### 4. Splitting the Data

The data is split into:
- A **training set** containing 80% of the data.
- A **test set** containing the remaining 20%.

### 5. Model Training and Evaluation

We train two models to predict the `average_rating`:
1. **Linear Regression (LR)**: A basic regression model.
2. **Random Forest Regressor (RFR)**: A more complex ensemble learning method.

Both models are trained using the training set, and predictions are made on the test set. The Mean Squared Error (MSE) is computed to evaluate the performance of each model.

### 6. Making Predictions

We make predictions for:
- The **first row** in the test set.
- The **1000th row** in the test set.

The predicted ratings are compared to the real ratings to evaluate the models' accuracy.

## Results

The models' predictions for specific rows are printed, along with the real ratings from the test set. The Mean Squared Error (MSE) for both models is calculated and displayed to assess the models' performance.

## Libraries Used

- `pandas`: For data manipulation and analysis.
- `matplotlib`: For creating visualizations like histograms and plots.
- `seaborn`: For creating heatmaps to visualize correlations.
- `scikit-learn`: For machine learning algorithms and model evaluation (Linear Regression, Random Forest Regressor, Mean Squared Error).

## Conclusion

This project demonstrates how to preprocess data, train machine learning models, and evaluate their performance in predicting the average ratings of games. The models' prediction accuracy can be further improved by tuning hyperparameters or using more advanced algorithms.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.
