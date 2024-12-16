# Flower Classification Project

This project focuses on classifying different types of flowers using machine learning techniques. We use the well-known **Iris dataset** to train and evaluate multiple classification models, including **Logistic Regression (LR)**, **K-Nearest Neighbors (KNN)**, and **Support Vector Machine (SVM)**.

## Table of Contents
- [Overview](#overview)
- [Installation](#installation)
- [Usage](#usage)
- [Models and Evaluation](#models-and-evaluation)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Overview

The Iris dataset contains 150 instances, each representing a type of flower. The features include measurements of sepal length, sepal width, petal length, and petal width. The goal is to classify the flowers into three classes based on these features:

- Setosa
- Versicolor
- Virginica

I trained three classification models to predict the flower class based on the features and evaluated their performance using **cross-validation** and metrics like **accuracy**, **precision**, **recall**, and **F1-score**.

## Installation

To run this project locally, follow these steps:

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/flower-classification.git

2. Navigate to the project directory:
cd flower-classification

3. Create a virtual environment (optional but recommended):
python -m venv env

4.Activate the virtual environment:
On Windows:
.\env\Scripts\activate
On macOS/Linux:
source env/bin/activate

5. Install the required packages:
pip install -r requirements.txt

If you don't have a requirements.txt, you can install the dependencies manually:
pip install pandas matplotlib scikit-learn

## Usage

## To run the project and see the results, execute the following in the Jupyter Notebook or Python script:

### 1. Load and Preprocess Data:
- Load the Iris dataset from the UCI repository.
- Split the data into features (X) and target labels (Y).

### 2. Train Models:
- Train three models: Logistic Regression, K-Nearest Neighbors, and Support Vector Machine.
- Evaluate the models using cross-validation and accuracy metrics.

### 3. Evaluate Performance:
- Print the classification report (precision, recall, F1-score).
- Visualize the feature relationships using scatter matrix and histograms.

## Models and Evaluation

The following models were trained and evaluated on the dataset:

- **Logistic Regression (LR):** A linear model for binary and multiclass classification.
- **K-Nearest Neighbors (KNN):** A non-parametric method that classifies data based on the majority class of its nearest neighbors.
- **Support Vector Machine (SVM):** A powerful classification algorithm that finds the optimal hyperplane to separate classes.

I used **cross-validation** (10-fold) to evaluate the models' performance and reported their mean accuracy and standard deviation.

## Results

### Model Performance

| Model                  | Accuracy  | Mean Accuracy | Standard Deviation | Precision (Iris-setosa) | Precision (Iris-versicolor) | Precision (Iris-virginica) | Recall (Iris-setosa) | Recall (Iris-versicolor) | Recall (Iris-virginica) | F1-Score (Iris-setosa) | F1-Score (Iris-versicolor) | F1-Score (Iris-virginica) |
|------------------------|-----------|---------------|---------------------|-------------------------|----------------------------|--------------------------|-----------------------|--------------------------|--------------------------|--------------------------|----------------------------|----------------------------|
| **Logistic Regression** | 96.67%    | 97.5%         | 5.3%                | 1.00                    | 1.00                       | 0.92                     | 1.00                  | 0.91                     | 1.00                     | 1.00                     | 0.95                       | 0.96                       |
| **K-Nearest Neighbors** | 93.33%    | 97.5%         | 3.8%                | 1.00                    | 1.00                       | 0.85                     | 1.00                  | 0.82                     | 1.00                     | 1.00                     | 0.90                       | 0.92                       |
| **Support Vector Machine** | 96.67% | 95.8%         | 5.6%                | 1.00                    | 1.00                       | 0.92                     | 1.00                  | 0.91                     | 1.00                     | 1.00                     | 0.95                       | 0.96                       |

---

### Summary
- **Best Performing Model:** Logistic Regression and K-Nearest Neighbors performed equally well, achieving a mean accuracy of **97.5%**.
- **Performance on Iris Classes:** All models performed well across different classes, with near-perfect accuracy for Iris-setosa and Iris-virginica.
- **Evaluation Metrics:** Models were evaluated using **accuracy**, **precision**, **recall**, **F1-score**, and **support**.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
