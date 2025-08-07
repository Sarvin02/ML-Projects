# Anomaly Detection

This document summarizes the key points and findings from the `anomalyDetection.ipynb` notebook.

## Overview

Anomaly detection involves identifying data points, events, or observations that deviate significantly from the norm. This notebook demonstrates anomaly detection using the K-Nearest Neighbors (KNN) algorithm on a synthetic dataset.

## Dataset

- **Source**: The data is synthetically generated using the pyod.utils.data.generate_data` function.
- **Description**: A random dataset consisting of 300 data points with two features. 10% of the data points are generated as outliers.
- **Features**: Two numerical features, referred to as 'Feature 1' and 'Feature 2' in the analysis.

## Methodology

1. **Data Preprocessing**: No explicit data preprocessing steps such as handling missing values or feature scaling were performed as the data was synthetically generated and clean.

2. **Modeling**:
   - **Algorithm used**: K-Nearest Neighbors (KNN) from the PyOD library.
   - **Evaluation metric**: The number of prediction errors, which is the count of misclassified data points (inliers predicted as outliers and vice-versa).

3. **Hyperparameter Tuning**: No hyperparameter tuning was performed. The `contamination` parameter of the KNN model was set to `0.1`, which is the known fraction of outliers in the dataset.

## Results

- **Model**: K-Nearest Neighbors (KNN).
- **Performance**: The model's performance is evaluated by the number of prediction errors. The notebook calculates and prints this number. The notebook also visualizes the learned decision boundary for the outliers.

## Conclusion

The anomaly detection model using KNN was successfully trained on a synthetic dataset. The model's decision boundary was visualized to show how it separates inliers from outliers. The performance was measured by the number of misclassifications. For a more robust evaluation, one could use metrics like Precision, Recall, and F1-score on a labeled real-world dataset.

## References

- [PyOD: A Python Toolbox for Scalable Outlier Detection](https://github.com/yzhao062/pyod)
