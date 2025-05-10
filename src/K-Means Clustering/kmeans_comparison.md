K-Means Clustering Algorithm:
K-Means partitions data into K clusters by iteratively minimizing the distance between points and cluster centroids. 

GENERAL K-MEANS CLUSTERING ALGORITHM:
It works in 4 steps:
1. Initialize K random centroids
2. Assign points to the nearest centroid
3. Recalculate centroids as cluster means
4. Repeat until convergence

![Result of General K-Means Clustering Alogorithm:](https://github.com/Janaprasath/UAV-Assisted-Wireless-Coverage--Clustering-Algorithms-for-Optimized-UAV-Deployment/blob/main/src/K-Means%20Clustering/General%20K-Means%20Clustering%20Algorithm/Result%20of%20General%20K-Means%20Clustering%20Algorithm.png)


Number of users in each cluster determined by General K-Means Clustering Alogorithm:
Location of UAV determined by General K-Means Clustering Alogorithm:

Drawbacks of General K-Means for UAV Deployment:
1. Unbalanced clusters: Standard K-Means often creates oversized clusters (>100 users), violating UAV capacity limits (Fig. 3)
2. Fixed cluster count: Requires predefining K, but UAV availability may change dynamically
3. Noise sensitivity: Outliers distort centroid positions, affecting UAV placement accuracy
4. Spherical bias: Assumes circular clusters, struggling with real-world urban user distributions.

MODIFIED K MEANS CLUSTERING ALGORITHM:
A modified K-Means approach is proposed to address the issue of clusters exceeding the allowed user limit. This enhanced method incorporates additional constraints during clustering to ensure no cluster surpasses the 100-user threshold.

The constraint-aware version addresses these limitations through:
_________________________________________________________________________________
|  Feature	General          |    General K-Means	|      Modified K-Means       |
_________________________________________________________________________________
|  Cluster size limit	       |    ❌	            |     ✅ 100-user cap         |
|  Dynamic cluster count	   |    ❌ Fixed K	    |     ✅ Auto-adjusts         |
|  Centroid computation	     |    ✅	            |     ✅ Optimized for UAVs   |
_________________________________________________________________________________

