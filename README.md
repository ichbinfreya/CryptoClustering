# Cryptocurrency Clustering Analysis
## Project Overview
This project applies unsupervised machine learning techniques to cluster various cryptocurrencies based on their price change percentages over different time periods. The primary goal is to explore the natural groupings of cryptocurrencies and understand the impact of dimensionality reduction using Principal Component Analysis (PCA) on the clustering results.

## Methodology
The project leverages the K-Means clustering algorithm, a popular unsupervised learning technique used to partition data into distinct clusters based on feature similarity. I perform clustering on both the original feature space and a reduced-dimensional space obtained using PCA to assess the impact of feature reduction on clustering performance.

### Key Steps
1. Data Preprocessing:
Normalization: The data is normalized using StandardScaler to ensure that all features contribute equally to the clustering process.
Feature Engineering: Price change percentages over different time frames (24h, 7d, 14d, etc.) are used as features.

2. Finding the Optimal Number of Clusters (k):
The optimal value of k is determined using the Elbow Method. The inertia (sum of squared distances of samples to their nearest cluster center) is calculated for different values of k.
An "elbow" in the inertia plot indicates the point where adding more clusters offers diminishing returns in terms of reducing inertia.

3. K-Means Clustering:
The K-Means algorithm is applied to both the original and PCA-transformed data to identify clusters of cryptocurrencies with similar behaviors.
Cluster labels are generated for each cryptocurrency, and results are visualized using scatter plots.

4. Dimensionality Reduction with PCA:
Principal Component Analysis (PCA) is used to reduce the dimensionality of the dataset, capturing the most significant variance in fewer components.
The impact of PCA on clustering is analyzed by comparing the clustering results of the original and reduced-dimensional data.

### Key Concepts
**Unsupervised Learning**:
Unsupervised learning involves training a model without labeled data to discover hidden patterns or groupings in the data. In this project, K-Means clustering is used to group cryptocurrencies without prior knowledge of their categories.

**K-Means Clustering**:
Objective: Partition the data into k clusters where each data point belongs to the cluster with the nearest mean.
Inertia: Measures the compactness of clusters. Lower inertia indicates tighter and more distinct clusters.
Choosing k: The Elbow Method is used to select the optimal number of clusters by plotting k values against inertia.

**Principal Component Analysis (PCA)**:
The purpose is to reduces the number of features while retaining the most significant variance in the data.
Advantage: Simplifies the clustering process by removing noise and redundant information, leading to better-defined clusters.

**Explained Variance**: Represents the proportion of the dataset's total variance captured by each principal component.


## Results and Observations
Original Data Clustering: Clustering in the original feature space revealed distinct clusters, but with some overlap, indicating the presence of noise or redundant features.

PCA Data Clustering: Clustering in the PCA-reduced space showed clearer, more defined clusters. This suggests that PCA successfully reduced noise and focused on the most informative aspects of the data.

## Comparison: The clusters formed in the PCA space were more compact and well-separated, demonstrating the advantage of using PCA before applying K-Means clustering.

### Advantages of Using PCA in Clustering
* Enhanced Cluster Separation: PCA helps to separate clusters more distinctly by focusing on the key variances in the data.
* Noise Reduction: By eliminating less important features, PCA reduces the noise in the data, resulting in more robust clusters.
* Computational Efficiency: Fewer features mean fewer computations, making the clustering process faster and more efficient.
* Visualization: PCA transforms high-dimensional data into 2D or 3D spaces, making it easier to visualize and interpret the clustering results.

How to Run the Project
* Install Dependencies: Ensure you have Python installed along with the necessary libraries: pandas, numpy, scikit-learn, matplotlib, and hvplot.
* Install the required libraries using: 

```
git bash 
pip install pandas numpy scikit-learn matplotlib hvplot
```

* Run the Analysis:
  Execute the Jupyter notebook or Python script to perform the clustering analysis and visualize the results.
* Visualize the Results:
  The final scatter plots and inertia plots will be generated as output, showing the clustering of cryptocurrencies in both the original and PCA-reduced spaces.

# Conclusion
This project demonstrates the effectiveness of combining PCA with K-Means clustering for improved cluster analysis. By reducing dimensionality and focusing on the most significant features, PCA enhances the clarity and interpretability of the clusters. This approach can be applied to various domains where high-dimensional data poses challenges for traditional clustering methods.
