# K-Means Clustering on Jewellery Dataset

This project aims to cluster a dataset of jewellery items using the K-Means clustering algorithm. The workflow includes data loading, scaling, determining the optimal number of clusters using the elbow method, clustering, visualization, and evaluation using silhouette scores.

## Project Description

### Data Loading

The dataset is loaded using pandas, and an initial exploration is done to understand the structure and content of the data.

### Data Preprocessing

#### Scaling with MinMaxScaler

The features are scaled using MinMaxScaler to ensure they are within the same range. This step is crucial for K-Means clustering to ensure that all features contribute equally to the result.

### Determining the Optimal Number of Clusters

#### Elbow Method

The elbow method is used to determine the optimal number of clusters by fitting K-Means with different numbers of clusters and plotting the within-cluster sum of squares (WCSS). The optimal number of clusters is identified where the plot shows an "elbow," indicating a point of diminishing returns.

The optimal number of clusters is further identified using the KneeLocator, which helps pinpoint the exact location of the "elbow" in the WCSS plot.

### K-Means Clustering

K-Means clustering is performed with the optimal number of clusters determined from the elbow method. The dataset is clustered, and a new column 'clusters' is added to the dataframe to indicate the cluster assignment for each data point.

### Visualization

The clusters are visualized using a pairplot to observe the distribution of data points in different clusters. This helps in understanding the separation and cohesion of clusters visually.

The cluster centroids are also identified and scaled back to the original feature space for interpretation. This provides insights into the central characteristics of each cluster.

### Evaluation

#### Silhouette Score

The silhouette score is used to evaluate the clustering performance for different numbers of clusters. The silhouette score measures how similar a data point is to its own cluster compared to other clusters. Higher silhouette scores indicate better-defined clusters.

Silhouette scores for a range of cluster numbers are plotted to help identify the optimal number of clusters that maximize the silhouette score.

## Usage

1. **Clone the repository**:
    ```bash
    git clone https://github.com/abhiram-k-2223/kmeans-clustering-jewels.git
    cd kmeans-clustering-jewels
    ```

2. **Install dependencies**:
    ```bash
    pip install pandas scikit-learn matplotlib seaborn kneed
    ```

3. **Run the Jupyter notebook or script**:
    - If using a Jupyter notebook, open `kmeans_clustering.ipynb` and run the cells sequentially.

4. **Output**:
    - Elbow plot showing WCSS for different numbers of clusters.
    - Optimal number of clusters identified using the elbow method.
    - Pairplot visualizing the clusters.
    - Cluster centroids in the original feature space.
    - Silhouette scores for different numbers of clusters.

This project demonstrates how to preprocess data, determine the optimal number of clusters, perform K-Means clustering, visualize the results, and evaluate clustering performance.
