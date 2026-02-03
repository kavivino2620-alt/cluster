# cluster
Evaluating K-Means Clustering: Custom vs. Scikit-Learn
This project demonstrates a fundamental implementation of the K-Means Clustering algorithm using NumPy. It provides a comparative analysis against the scikit-learn library, focusing on how centroid initialization impacts clustering performance through metrics like Within-Cluster Sum of Squares (WCSS) and the Silhouette Score.
🚀 Features
Custom K-Means Implementation: Manual logic for centroid initialization, Euclidean distance-based cluster assignment, and iterative centroid updates.
Synthetic Data Generation: Uses make_blobs to create a controlled environment with 4 distinct clusters for testing.
Performance Metrics:
WCSS (Inertia): Measures the total squared distance between each point and its assigned cluster center.
Silhouette Score: Evaluates how similar an object is to its own cluster compared to other clusters.
Initialization Sensitivity: Runs the custom algorithm with multiple random seeds to observe the effects of initial centroid placement.
📊 Results Summary
The evaluation shows that K-Means is sensitive to its starting state. While the custom implementation can match scikit-learn's performance, it requires a "lucky" initialization (e.g., Seed 10) to avoid local optima.
Key Takeaway
Our custom implementation achieved the exact same optimal WCSS and Silhouette Score as scikit-learn when using Seed 10. This highlights that the core logic is sound, but professional libraries like scikit-learn use more advanced initialization techniques (like k-means++) to consistently reach the best result.
