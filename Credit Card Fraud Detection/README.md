# Credit Card Fraud Detection

This notebook provides an implementation of machine learning algorithms for detecting fraudulent transactions in credit card data. It utilizes various anomaly detection models, including Isolation Forest, Local Outlier Factor (LOF), and Support Vector Machine (SVM).

## Overview

The dataset used in this notebook contains anonymized credit card transaction data with a target variable (`Class`) indicating whether a transaction is fraudulent (`1`) or valid (`0`). The notebook employs data preprocessing, correlation analysis, and machine learning techniques to classify transactions.

## Features

- **Data Loading and Exploration**:
  - Load the credit card dataset (`creditcard.csv`).
  - Analyze dataset structure and summary statistics.
  - Visualize histograms for feature distributions.

- **Outlier Detection Algorithms**:
  - **Isolation Forest**:
    - Detects anomalies by isolating instances in the data.
  - **Local Outlier Factor (LOF)**:
    - Detects anomalies based on local density deviation.
  - **Support Vector Machine (SVM)**:
    - Implements a one-class SVM for anomaly detection.

- **Performance Metrics**:
  - Precision, Recall, F1-Score, and Accuracy.
  - Comparisons between models on downsampled and full datasets.

- **Visualization**:
  - Histograms for feature distributions.
  - Heatmap of feature correlations.

## Installation

Before running the notebook, ensure you have the following Python libraries installed:

- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`
- `scikit-learn`

You can install the required libraries using pip:

```python
pip install numpy pandas matplotlib seaborn scikit-learn
```

## Dataset

Dataset used can be found on Kaggle on this link: https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

## Usage

1. **Load the Dataset**:  
   Place the `creditcard.csv` file in the same directory as the notebook.

2. **Run the Notebook**:  
   Execute the cells in the notebook sequentially to:
   - Load and preprocess the dataset.
   - Train and evaluate models.
   - View performance metrics and visualizations.

3. **Modify the Sample Size**:  
   Adjust the `frac` parameter in the following line to change the dataset size for quicker processing:  
   ```python
   data_4_svm = data.sample(frac=0.15, random_state=1)

## Key Outputs

### 1. **Model Performance**
Each model provides the following metrics:
- **Number of Errors**: Misclassified transactions (fraud or valid).
- **Accuracy**: Proportion of correct predictions.
- **Precision**: Proportion of correctly identified positive cases out of all predicted positives.
- **Recall**: Proportion of actual positive cases correctly identified.
- **F1-Score**: Harmonic mean of precision and recall.

### 2. **Correlation Matrix**
- A heatmap visualization shows the correlation between features, helping identify relationships in the dataset.  
  Example:  
  - Features with higher correlations may indicate potential areas for further analysis.

### 3. **Transaction Breakdown**
- **Fraud Cases**: Total number of fraudulent transactions.
- **Valid Transactions**: Total number of non-fraudulent transactions.
- **Outlier Fraction**: Ratio of fraudulent transactions to valid transactions.

### 4. **Visualizations**
- **Histograms**: Distribution of each feature across the dataset.
- **Heatmap**: Correlation matrix for feature analysis.

### 5. **Downsized Dataset Results**
- Model performance on a reduced dataset (15% sample) for computational efficiency.
- Results include metrics for:
  - Isolation Forest
  - Local Outlier Factor
  - Support Vector Machine

## Notes

1. This project uses the `creditcard.csv` dataset, which contains anonymized transaction data to protect sensitive information.
2. The dataset includes:
   - PCA-transformed features (V1 to V28).
   - `Time` and `Amount` features for temporal and monetary insights.
   - `Class` as the target variable, where `1` indicates fraud and `0` indicates a valid transaction.
3. Models utilized for fraud detection:
   - Isolation Forest: Unsupervised anomaly detection.
   - Local Outlier Factor (LOF): Local density-based detection for novelty or anomaly.
   - Support Vector Machine (SVM): One-class SVM for identifying abnormal patterns.
4. The dataset is highly imbalanced, with a small fraction of transactions being fraudulent. This necessitates careful handling of metrics and model performance evaluations.
5. Outputs include performance metrics, visualizations, and a correlation matrix to aid feature analysis.
6. The LocalOutlierFactor classifier is used with novelty=True for decision function compatibility.

## License

This project is licensed under the MIT License.
