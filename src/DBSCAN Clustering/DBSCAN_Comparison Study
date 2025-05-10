DBSCAN CLUSTERING:
- DBSCAN (Density-Based Spatial Clustering of Applications with Noise) groups users based on spatial density, identifying core points (high-density regions), border points, and noise points

 GENERAL DBSCAN CLUSTERING ALGORITHM:
It operates in 3 steps:
1. Identify core points (points with ≥ min_samples neighbors within distance eps).
2. Expand clusters by connecting density-reachable core points.
3. Label outliers as noise.

![Result of General DBSCAN Clustering Alogorithm:](https://github.com/Janaprasath/UAV-Assisted-Wireless-Coverage--Clustering-Algorithms-for-Optimized-UAV-Deployment/blob/main/src/DBSCAN%20Clustering/General%20DBSCAN%20Clustering%20Algorithm/Result%20of%20General%20DBSCAN%20Clustering%20Algorithm.png)
![Number of users in each cluster determined byGeneral K-Means Clustering Alogorithm:]
![Location of UAV determined by General K-Means Clustering Alogorithm:]


Drawbacks of General DBSCAN for UAV Deployment
1. Uncontrolled cluster sizes: Density-based merging often creates oversized clusters (e.g.150 users), violating UAV capacity.
2. Noise neglect: Up to 15% of users are labeled as noise (unclustered), leaving them without coverage.
3. No centroid computation: Provides cluster labels but no UAV deployment coordinates.
4. Parameter sensitivity: Poor eps or min_samples choices lead to under/over-clustering. 
