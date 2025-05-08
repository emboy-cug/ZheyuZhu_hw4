# Homework 4: Machine Learning Clustering Tasks

This repository contains solutions for Homework 4, focusing on machine learning clustering tasks. The primary objective is to apply clustering algorithms like **Hierarchical Clustering** and **K-Means Clustering** to analyze datasets. The datasets used in this project include the **Auto-MPG**, **Boston Housing**, and **Wine** datasets.

## Problem 1: Hierarchical Clustering of Auto-MPG Dataset

### Objective:
In this task, hierarchical clustering is applied to the Auto-MPG dataset, which includes continuous features such as miles per gallon (mpg), displacement, horsepower, weight, and acceleration. The goal is to analyze the clustering results and explore the relationship between the clusters and the origin class labels.

### Steps:
1. **Load the Auto-MPG dataset**: The dataset is loaded from a CSV or other file format.
2. **Handle missing data**: Any missing values in the dataset are imputed using the mean value for each feature.
3. **Standardize the features**: All features are standardized using standard scaling to ensure that they are on the same scale.
4. **Perform Hierarchical Clustering**: The clustering is performed using the **average linkage method** with **Euclidean distance**.
5. **Compute mean and variance for each cluster**: After clustering, the mean and variance for each feature within each cluster are calculated.
6. **Compare cluster statistics with origin class labels**: The resulting clusters are compared with the origin class labels to evaluate the clustering's effectiveness.

### Output:
- **Cluster Mean and Variance Values for Features**: Tables displaying the mean and variance of features within each cluster, both for standardized and original data.
- **Crosstab of Cluster Assignments and Origin Classes**: A crosstab table showing how each cluster relates to the origin class labels.

## Problem 2: K-Means Clustering Analysis on the Boston Dataset

### Objective:
This task applies **K-Means clustering** to the **Boston Housing dataset** to determine the optimal number of clusters. The objective is to maximize the **Silhouette score** for clustering, and after finding the optimal number of clusters, the feature means and centroids of the clusters are analyzed.

### Steps:
1. **Load the Boston housing dataset**: The dataset is loaded and processed to analyze housing data in Boston.
2. **Standardize the features**: Each feature is standardized to ensure equal weighting in the clustering algorithm.
3. **Perform K-Means clustering**: K-Means clustering is applied with different values of `k` (ranging from 2 to 6).
4. **Compute Silhouette scores**: Silhouette scores are calculated to determine the optimal number of clusters, based on how well-separated the clusters are.
5. **Compute cluster means and centroids**: The mean values of features within each cluster are calculated and compared with the centroids of the clusters.
6. **Visualize clustering results**: The results of clustering are visualized, including a **pairplot** and **PCA** plots to understand how the data points are distributed across clusters.

### Output:
- **Silhouette Scores for Different k Values**: A table and plot showing the Silhouette scores for various cluster sizes (`k` values).
- **Cluster Means and Centroids**: Tables showing the mean values and centroids for each cluster.
- **Cluster vs. Origin Crosstab**: A crosstab table comparing the clusters with the origin classes.

## Problem 3: K-Means Clustering Analysis on the Wine Dataset

### Objective:
This task uses **K-Means clustering** on the **Wine dataset** to compute clustering metrics such as **Homogeneity**, **Completeness**, **V-Measure**, and the **Adjusted Rand Index (ARI)**. The goal is to evaluate how well the clustering reflects the true wine classes.

### Steps:
1. **Load the Wine dataset**: The dataset containing wine characteristics is loaded for analysis.
2. **Standardize the features**: The features are standardized to ensure that they contribute equally to the clustering process.
3. **Perform K-Means clustering with k=3**: K-Means clustering is performed with `k=3` clusters, reflecting the three types of wine in the dataset.
4. **Calculate Homogeneity and Completeness**: These metrics are calculated to evaluate the clustering performance, determining how well the clusters correspond to true wine classes.
5. **Compute cluster means and centroids**: The means and centroids of the features are computed for each cluster.
6. **Visualize the clustering results**: Visualizations such as **PCA plots** and **pairplots** are generated to illustrate the clustering.

### Output:
- **Homogeneity and Completeness Scores**: Metrics evaluating how well the clustering aligns with the true classes.
- **Cluster Means and Centroids**: Tables of feature means and centroids for each cluster.
- **Visualizations**: **PCA** and **Pairplot** visualizations of the clusters.

## Installation

To run the code in this repository, you will need to install the following Python libraries:

```bash
pip install numpy pandas scikit-learn matplotlib seaborn ucimlrepo
