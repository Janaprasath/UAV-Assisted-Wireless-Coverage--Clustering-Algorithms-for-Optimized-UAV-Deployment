# UAV-Assisted Wireless Coverage: Clustering Algorithms for Optimized UAV Deployment

OVERVIEW:
1.This project implements and analyzes clustering algorithms for optimizing the deployment of Unmanned Aerial Vehicles (UAVs) as wireless communication relays, particularly in scenarios where terrestrial infrastructure is unavailable or compromised (e.g., disaster recovery, rural connectivity, smart cities). 
2.The focus is on ensuring efficient user coverage, balanced resource allocation, and adherence to operational constraints such as user capacity per UAV.

PROBLEM STATEMENT:
1.UAVs are increasingly deployed as temporary communication relays in challenging environments. However, maximizing their effectiveness requires:
2.Optimal placement to maximize coverage and minimize interference.
3.Efficient clustering of users to balance UAV loads and reduce power consumption.
Adherence to constraints such as maximum users per UAV and limited UAV resources.

KEY FEATURES:
1.Implements and compares six algorithms: General and modified versions of K-Means, DBSCAN, and Hierarchical Agglomerative Clustering.
2.Constraint-aware clustering: Modified algorithms enforce a strict user capacity limit per UAV, reflecting real-world operational requirements.
3.Simulation and analysis: Evaluates algorithm performance on a densely distributed urban user dataset.
4.Centroid computation: Modified algorithms include mechanisms for calculating UAV deployment locations.
5.Comprehensive documentation: Includes problem background, algorithm pseudocode, simulation results, and references.

Experimental Setup:
1.Dataset: 1014 users distributed in a 1000×1000 m² urban region.
2.UAV parameters: Each UAV operates at 150m altitude and can serve up to 100 users.
3.The user location data points were first compiled and loaded into an Excel sheet to ensure structured data management and facilitate easy import into the clustering algorithms
