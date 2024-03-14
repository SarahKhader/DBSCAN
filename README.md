# DBSCAN
Density based clustering basic implementation

This implementation creates a DBSCAN class with parameters eps (maximum distance between two samples for them to be considered as in the same neighborhood) and min_samples (minimum number of samples in a neighborhood for a point to be considered as a core point). It then has a fit method to fit the DBSCAN algorithm to the data. The region_query method finds all points within the eps distance of a given point. The expand_cluster method expands a cluster by recursively adding core points and their neighbors to the cluster. Finally, the distance method calculates the Euclidean distance between two points.

some cosiderations for the fitness function
Compactness,Separation: Increase the distances between different clusters. To achieve this, it calculates: Intra-cluster variance: Measures the spread of data points within each cluster. Inter-cluster distance: Measures the distance between different clusters.
Noise points ,Silhouette Score: The silhouette score is a metric that combines the average within-cluster distance and the average nearest-cluster distance. Maximizing the silhouette score indicates well-separated clusters with similar intra-cluster distances.
