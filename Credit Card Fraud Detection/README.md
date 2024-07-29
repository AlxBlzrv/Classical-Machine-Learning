# Credit Card Fraud Detection

## Overview

This project aims to detect fraudulent transactions in credit card data using anomaly detection techniques. The dataset used is the [Credit Card Fraud Detection](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud) dataset from Kaggle. The primary goal is to build a Logistic Regression model to classify transactions as either fraudulent or non-fraudulent.

## Features

- **Data Exploration:** Analyze and visualize the data distribution and correlation matrix.
- **Data Preprocessing:** Normalize the 'Amount' column and perform undersampling to handle class imbalance.
- **Model Training:** Train a Logistic Regression model on the undersampled data.
- **Evaluation:** Evaluate the model using various metrics and plots, including confusion matrix, ROC curve, and Precision-Recall curve.

## Setup

### Prerequisites

Ensure you have the following Python packages installed:

- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`
- `scikit-learn`

You can install these packages using pip:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

### Dataset

Download the dataset from [Kaggle](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud) and place it in the appropriate directory.

## Usage

1. **Load the Dataset**

   ```python
   import pandas as pd

   data = pd.read_csv('/path/to/creditcard.csv')
   ```

2. **Data Exploration and Visualization**

   - Plot the correlation matrix.
   - Visualize data distributions before and after normalization.

3. **Data Preprocessing**

   - Normalize the 'Amount' column.
   - Perform undersampling to balance the dataset.

4. **Model Training**

   ```python
   from sklearn.linear_model import LogisticRegression

   lr = LogisticRegression(C=0.01, penalty='l1', solver='liblinear')
   lr.fit(X_train_undersample, y_train_undersample.values.ravel())
   ```

5. **Evaluation**

   - Plot and interpret the confusion matrix.
   - Plot the ROC curve and compute AUC.
   - Plot the Precision-Recall curve and evaluate model performance using precision, recall, and F1-score.

## Metrics

- **AUC (Area Under the Curve):** Measures the performance of the ROC curve; a higher AUC indicates better model performance.
- **Precision:** The ratio of true positive predictions to the total number of positive predictions. Indicates how many of the predicted frauds are actual frauds.
- **Recall:** The ratio of true positive predictions to the total number of actual positives. Indicates how many of the actual frauds are correctly identified.
- **F1-Score:** The harmonic mean of Precision and Recall. Useful for balancing Precision and Recall in scenarios with imbalanced classes.
- **ROC Curve:** Plots the True Positive Rate against the False Positive Rate for various thresholds.
- **Precision-Recall Curve:** Plots Precision against Recall for various thresholds.

## Contributing

Feel free to open issues or submit pull requests if you have suggestions or improvements for this project.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [Kaggle](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud) for providing the dataset.
- [Scikit-learn](https://scikit-learn.org/) for the machine learning tools and metrics.
