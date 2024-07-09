# Hierarchical-Clustering
## Abstract:
Clustering is one of the popular techniques used to create homogeneous groups of entities or objects. For a given set of data points, grouping the data points into X number of clusters so that similar data points in the clusters are close to each other. Hierarchical clustering creates clusters in a hierarchical tree-like structure (also called a Dendrogram). Meaning, a subset of similar data is created in a tree-like structure in which the root node corresponds to the entire data, and branches are created from the root node to form several clusters.
 
## Objective:
The hierarchical clustering algorithm aims to find nested groups of the data by building the hierarchy. It is similar to the biological taxonomy of the plant or animal kingdom. Hierarchical clusters are generally represented using the hierarchical tree known as a dendrogram.

## Introduction:
The sole concept of hierarchical clustering lies in just the construction and analysis of a dendrogram. A dendrogram is a tree-like structure that explains the relationship between all the data points in the system. However, like a regular family tree, a dendrogram need not branch out at regular intervals from top to bottom as the vertical direction (y-axis) in it represents the distance between clusters in some metric. As you keep going down in a path, you keep breaking the clusters into smaller and smaller units until your granularity level reaches the data sample. In the vice versa situation, when you traverse in up direction, at each level, you are subsuming smaller clusters into larger ones till the point you reach the entire system. As a result, hierarchical clustering is also known as clustering of clustering. There are two ways of constructing it. One way to construct it is by bottoms-up where you start from the bottom and keep merging the individual data points and subclusters and go all the way to the top. This is known as agglomerative clustering. The other alternative is the opposite procedure of top-down in which you start by considering the entire system as one cluster and then keep sub clustering it until you reach individual data samples. This process is known as divisive clustering. Each of these methods has separate algorithms to achieve its objectives.

### a) Agglomerative clustering
One of the simplest and easily understood algorithms used to perform agglomerative clustering is single linkage. In this algorithm, we start with considering each data point as a subcluster. We define a metric to measure the distance between all pairs of subclusters at each step and keep merging the nearest two subclusters in each step. We repeat this procedure till there is only one cluster in the system.

### b) Divisive clustering
One of the algorithms used to perform divisive clustering is recursive k-means. As the name suggests, you recursively perform the procedure of k-means on each intermediate cluster till you encounter all the data samples in the system or the minimum number of data samples you desire to have in a cluster. In each step of this algorithm, you have to be mindful of how many clusters would you like to create next.
 
 ## Methodology :
 The basic algorithm of Agglomerative is :
 1. Compute the proximity matrix
 2. Let each data point be a cluster
 3. Repeat: Merge the two closest clusters and update the proximity matrix until only a single cluster remains

Key operation is the computation of the proximity of two clusters.
 The basic algorithm of Divisive is :
 - given a dataset (d1, d2, d3, ....dN) of size N
 - at the top we have all data in one cluster
 - the cluster is split using a flat clustering method eg. K-Means etc
 - repeat
 - choose the best cluster among all the clusters to split
 - split that cluster by the flat clustering algorithm until each data is in its own single cluster.

 ## Conclusion:
 Hierarchical clustering is a very useful way of segmentation. It has been adopted for categorical knowledge and its useful because of its versatility. The advantage of not having to pre-define the number of clusters give it quite an edge over k-means. It has numerous applications like image segmentation, object recognition and data filtering and retrieval. However, it doesn’t work well when we have huge amount of data.
