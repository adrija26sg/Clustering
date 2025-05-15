# Clustering Analysis on Seeds Dataset

This project explores clustering techniques on the Seeds dataset using various preprocessing methods. We evaluate the performance of K-Means, Hierarchical Clustering, and KMeans Shift, alongside different levels of data preprocessing such as normalization, transformation, and PCA.



## 📊 Dataset
- **Name**: Seeds Dataset  
- **Source**: UCI Machine Learning Repository

The dataset consists of measurements of geometrical properties of kernels belonging to three different varieties of wheat. This dataset has been used for classification and clustering tasks.

## 🧪 Clustering Techniques
The following clustering algorithms were applied:

- **K-Means Clustering**
- **Hierarchical Clustering**
- **KMeans Shift Clustering**

## ⚙️ Preprocessing Approaches
Each algorithm was tested under four preprocessing scenarios to understand the effect of different preprocessing techniques on the clustering results:

 - **No Preprocessing:**
No transformation or normalization was applied to the raw data.

- **Normalization Only**
The data was scaled to a specific range (typically 0 to 1) to ensure equal contribution of features in clustering.

- **Transformation + Normalization (T+N):**
Data transformation (e.g., log transformation) was applied before normalization to handle skewed distributions.

- **Transformation + Normalization + PCA (T+N+PCA):**
Data transformation and normalization were followed by Principal Component Analysis (PCA) for dimensionality reduction, which helps in reducing noise and capturing the most important features of the data.

## 🏆 Results
| Criterion | Best Result |
|----------|-------------|
| **Best Clustering Algorithm** | K-Means (with T+N+PCA) |
| **Best Number of Clusters** | 3 |
| **Best Silhouette Score** | ~0.32 (K-Means with T+N+PCA) |

K-Means consistently performed well across all preprocessing combinations, with the best performance seen when using Transformation + Normalization + PCA (T+N+PCA). This preprocessing combination resulted in the highest silhouette score, which indicates that the clusters formed were well-separated.

## 📈 Visualizations
The clustering results were visualized using 2D projections after applying PCA to reduce the dimensionality of the data. This allowed us to effectively demonstrate the separation between clusters across different techniques and preprocessing steps.

## 🧠 Conclusion
- **K-Means clustering** proved to be the most reliable and effective algorithm, especially when used with full preprocessing (T+N+PCA). The algorithm consistently gave the best results, with a well-formed cluster structure and the highest silhouette score.

- **Hierarchical Clustering** improved with normalization but did not outperform K-Means. While it showed potential, the results were less stable compared to K-Means.

- **KMeans Shift** worked decently without preprocessing but had higher computational costs, which might be a limitation when working with large datasets.

- **Optimal clustering** was achieved with 3 clusters, which matches the expected number of seed types in the dataset. This supports the hypothesis that the seeds dataset can be effectively grouped into three distinct clusters.

- **Silhouette analysis** confirmed the quality of clustering, with the best score achieved using K-Means after full preprocessing. A higher silhouette score indicates that the data points are well-matched within their clusters and distinct from other clusters.

## 📄 PDF Report
A full breakdown of results and metrics is available in the [PDF report](https://github.com/adrija26sg/Clustering/blob/main/Results_Clustering%20.pdf.pdf)
