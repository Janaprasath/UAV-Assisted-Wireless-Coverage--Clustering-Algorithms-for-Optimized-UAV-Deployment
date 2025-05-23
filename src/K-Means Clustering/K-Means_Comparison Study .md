K-MEANS CLUSTERING ALGORITHM:
- K-Means partitions data into K clusters by iteratively minimizing the distance between points and cluster centroids. 

GENERAL K-MEANS CLUSTERING ALGORITHM:
- It works in 4 steps:
1. Initialize K random centroids
2. Assign points to the nearest centroid
3. Recalculate centroids as cluster means
4. Repeat until convergence

![Result of General K-Means Clustering Algorithm:](https://github.com/Janaprasath/UAV-Assisted-Wireless-Coverage--Clustering-Algorithms-for-Optimized-UAV-Deployment/blob/main/src/K-Means%20Clustering/General%20K-Means%20Clustering%20Algorithm/Result%20of%20General%20K-Means%20Clustering%20Algorithm.png)

![Number of users in each cluster determined by General K-Means Clustering Algorithm:](https://github.com/Janaprasath/UAV-Assisted-Wireless-Coverage--Clustering-Algorithms-for-Optimized-UAV-Deployment/blob/main/src/K-Means%20Clustering/General%20K-Means%20Clustering%20Algorithm/Number%20of%20users%20in%20each%20cluster%20determined%20by%20General%20K-Means%20Clustering%20Algorithm.png)

![Location of UAV determined by General K-Means Clustering Algorithm:](https://github.com/Janaprasath/UAV-Assisted-Wireless-Coverage--Clustering-Algorithms-for-Optimized-UAV-Deployment/blob/main/src/K-Means%20Clustering/General%20K-Means%20Clustering%20Algorithm/Location%20of%20UAV%20determined%20by%20General%20K-Means%20Clustering%20Algorithm.png)


Drawbacks of General K-Means for UAV Deployment:
1. Unbalanced clusters: Standard K-Means often creates oversized clusters (>100 users), violating UAV capacity limits (Fig. 3)
2. Fixed cluster count: Requires predefining K, but UAV availability may change dynamically
3. Noise sensitivity: Outliers distort centroid positions, affecting UAV placement accuracy
4. Spherical bias: Assumes circular clusters, struggling with real-world urban user distributions.

MODIFIED K MEANS CLUSTERING ALGORITHM:
- A modified K-Means approach is proposed to address the issue of clusters exceeding the allowed user limit. This enhanced method incorporates additional constraints during clustering to ensure no cluster surpasses the 100-user threshold.

The constraint-aware version addresses these limitations through:

|  Feature	General          |    General K-Means	|      Modified K-Means       |
|----------------------------|--------------------|-----------------------------|
|  Cluster size limit	       |    ❌	            |     ✅ 100-user cap         |
|  Dynamic cluster count	   |    ❌ Fixed K	    |     ✅ Auto-adjusts         |
|  Centroid computation	     |    ✅	            |     ✅ Optimized for UAVs   |

![Result of Modified K-Means Clustering Algorithm:](https://github.com/Janaprasath/UAV-Assisted-Wireless-Coverage--Clustering-Algorithms-for-Optimized-UAV-Deployment/blob/main/src/K-Means%20Clustering/Modified%20K-Means%20Clustering%20Algorithm/Result%20of%20Modified%20K-Means%20Clustering%20Algorithm.png)


![Number of users in each cluster determined by Modified K-Means Clustering Algorithm:](https://github.com/Janaprasath/UAV-Assisted-Wireless-Coverage--Clustering-Algorithms-for-Optimized-UAV-Deployment/blob/main/src/K-Means%20Clustering/Modified%20K-Means%20Clustering%20Algorithm/Number%20of%20users%20in%20each%20cluster%20determined%20by%20the%20Modified%20K-Means%20Algorithm.png)

![Location of UAV determined by Modified K-Means Clustering Algorithm:](https://github.com/Janaprasath/UAV-Assisted-Wireless-Coverage--Clustering-Algorithms-for-Optimized-UAV-Deployment/blob/main/src/K-Means%20Clustering/Modified%20K-Means%20Clustering%20Algorithm/Location%20of%20UAV%20determined%20by%20Modified%20K-Means%20Clustering%20Algorithm.png)

- The proposed algorithm ensures that no cluster exceeds the predefined 100-user limit. Once clustering is complete, centroid values are computed to guide UAV deployment. By adhering to capacity constraints, this enhanced approach optimizes UAV allocation, maximizing operational efficiency and service coverage
