# Unsupervised Anomaly Detection on Hypothyroidism Dataset

This repository contains the implementation of multiple **unsupervised anomaly detection** algorithms applied to a hypothyroidism dataset. The **main goal** is to identify anomalous patient records using various methods and combine their outputs for enhanced accuracy through majority voting.

## Dataset

The dataset consists of 7,200 records with 21 attributes, of which 15 are binary and 6 are continuous. It is related to hypothyroidism, a condition that occurs when the thyroid gland is underactive. The dataset was preprocessed to handle duplicates, normalize features, and compute distances for mixed data types.

## Methods Used

1. **K-Nearest Neighbors (KNN):**
   - A proximity-based algorithm that detects anomalies based on distance to the nearest neighbors.

2. **Local Outlier Factor (LOF):**
   - A density-based method that identifies anomalies in low-density regions.

3. **DBSCAN (Density-Based Spatial Clustering of Applications with Noise):**
   - A clustering algorithm that finds anomalies that do not belong to dense clusters.

4. **Principal Component Analysis (PCA):**
   - A reconstruction-based approach that identifies anomalies based on reconstruction error in lower-dimensional space.

5. **One-Class SVM (Support Vector Machine):**
   - A support vector method to learn the boundary of the normal class and identify outliers.

6. **Majority Voting:**
   - Combines the results of individual methods to enhance robustness by labeling records flagged as anomalous by at least three algorithms.

## Results

Anomalies detected by each algorithm are visualized in 2D and 3D space using PCA and t-SNE. The final anomaly labels are assigned based on the majority voting approach, identifying 5.9% of the dataset as anomalous.

### _Content_:
- [unsupervised_anomaly_detection.ipynb](https://github.com/MomiQB/Unsupervised-Anomaly-Detection/blob/main/unsupervised_anomaly_detection.ipynb): notebook implementing the analysis and the methodologies.
- [gower_distance_matrix.npy](https://github.com/MomiQB/Unsupervised-Anomaly-Detection/blob/main/gower_distance_matrix.npy): numpy file with Gower distances.


