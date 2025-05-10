DBSCAN CLUSTERING:
- DBSCAN (Density-Based Spatial Clustering of Applications with Noise) groups users based on spatial density, identifying core points (high-density regions), border points, and noise points

GENERAL DBSCAN CLUSTERING ALGORITHM:
It operates in 3 steps:
1. Identify core points (points with ≥ min_samples neighbors within distance eps).
2. Expand clusters by connecting density-reachable core points.
3. Label outliers as noise.

![Result of General DBSCAN Clustering Alogorithm:](https://github.com/Janaprasath/UAV-Assisted-Wireless-Coverage--Clustering-Algorithms-for-Optimized-UAV-Deployment/blob/main/src/DBSCAN%20Clustering/General%20DBSCAN%20Clustering%20Algorithm/Result%20of%20General%20DBSCAN%20Clustering%20Algorithm.png)

![Number of users in each cluster determined by General DBSCAN Clustering Alogorithm:](https://github.com/Janaprasath/UAV-Assisted-Wireless-Coverage--Clustering-Algorithms-for-Optimized-UAV-Deployment/blob/main/src/DBSCAN%20Clustering/General%20DBSCAN%20Clustering%20Algorithm/Number%20of%20users%20in%20each%20cluster%20determined%20by%20General%20DBSCAN%20Clustering%20Algorithm.png)

Drawbacks of General DBSCAN for UAV Deployment
1. Uncontrolled cluster sizes: Density-based merging often creates oversized clusters (e.g.150 users), violating UAV capacity.
2. Noise neglect: Up to 15% of users are labeled as noise (unclustered), leaving them without coverage.
3. No centroid computation: Provides cluster labels but no UAV deployment coordinates.
4. Parameter sensitivity: Poor eps or min_samples choices lead to under/over-clustering.

MODIFIED DBSCAN CLUSTERING ALGORITHM:

Feature                    |     General DBSCAN         |        Modified DBSCAN
---------------------------|----------------------------|--------------------------------------------|                        
Cluster size limit	        |     ❌	                    |       ✅ 100-user cap                      |
Noise handling	            |     ❌ Labels as noise	    |     ✅ Reassigns to nearest cluster        |
Centroid computation	      |     ❌                     |   	✅ Optimized UAV positions              |
Parameter adaptation	      |     ❌ Fixed eps	           |    ✅ Auto-tunes eps via k-distance graph |






- The modified DBSCAN algorithm strictly enforces the 100-user cluster limit.
- Additionally, it incorporates a function to efficiently manage noise points, reassigning them to appropriate clusters when feasible.
- A separate function computes centroid values, providing a representative central point for each cluster

![Result of Modified DBSCAN Clustering Alogorithm:](https://github.com/Janaprasath/UAV-Assisted-Wireless-Coverage--Clustering-Algorithms-for-Optimized-UAV-Deployment/blob/main/src/DBSCAN%20Clustering/Modified%20DBSCAN%20Clustering%20Algorithm/Result%20of%20Modified%20DBSCAN%20clustering%20Algorithm.png)

![Number of users in each cluster determined by Modified K-Means Clustering Alogorithm:](https://github.com/Janaprasath/UAV-Assisted-Wireless-Coverage--Clustering-Algorithms-for-Optimized-UAV-Deployment/blob/main/src/DBSCAN%20Clustering/Modified%20DBSCAN%20Clustering%20Algorithm/Number%20of%20users%20in%20each%20cluster%20determined%20by%20Modified%20DBSCAN%20clustering%20algorithm.png)


![Location of UAV determined by Modified DBSCAN Clustering Alogorithm:](https://github.com/Janaprasath/UAV-Assisted-Wireless-Coverage--Clustering-Algorithms-for-Optimized-UAV-Deployment/blob/main/src/DBSCAN%20Clustering/Modified%20DBSCAN%20Clustering%20Algorithm/Location%20of%20UAV%20determined%20by%20Modified%20DBSCAN%20clustering%20algorithm.png)

-The proposed modified DBSCAN algorithm enforces all specified constraints, effectively addressing the limitations of the standard DBSCAN approach. 
- By strictly capping each cluster at 100 users, efficiently reassigning noise points to suitable clusters, and computing centroid values, this enhanced method ensures balanced and efficient clustering.
-  As a result, it is well-suited for practical UAV deployment scenarios, where adherence to constraints and optimized clustering outcomes are critical for performance
