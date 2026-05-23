# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries and load the customer dataset.

2.Select Annual Income and Spending Score as input features for clustering.

3.Apply the K-Means algorithm to divide customers into 5 clusters.

4.Plot the clustered customers and display the cluster centroids on the graph.
## Program:
```

Program to implement the K Means Clustering for Customer Segmentation.
Developed by: KARTHIKEYAN A
RegisterNumber:  212225230131

```
```

import pandas as pd
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans

data = pd.read_csv("Mall_Customer.csv")

X = data.iloc[:, [3, 4]].values

kmeans = KMeans(n_clusters=5, random_state=0)

y_kmeans = kmeans.fit_predict(X)

plt.scatter(X[:, 0], X[:, 1], c=y_kmeans, s=50)

plt.scatter(kmeans.cluster_centers_[:, 0],
            kmeans.cluster_centers_[:, 1],
            s=200,
            marker='X')

plt.xlabel("Annual Income")
plt.ylabel("Spending Score")
plt.title("Customer Segmentation using K-Means")

plt.show()
```
## Output:
<img width="655" height="524" alt="image" src="https://github.com/user-attachments/assets/5e657d83-59cc-4144-9d40-2e548bff902b" />

## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
