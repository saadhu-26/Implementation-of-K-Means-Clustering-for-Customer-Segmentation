# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:

To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

1.Import required libraries and load the customer dataset.

2.Select important features like Annual Income and Spending Score.

3.Apply K-Means clustering algorithm to group customers.

4.Visualize clusters and analyze customer segments.

## Program:
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: SAADHANA A
RegisterNumber: 25018432 
*/
```
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans

data = pd.read_csv(r"C:\Users\acer\Downloads\Mall_Customers.csv")   
print("Dataset Loaded Successfully\n")
print(data.head())

X = data[['Annual Income (k$)', 'Spending Score (1-100)']]

kmeans = KMeans(n_clusters=5, random_state=0)
y_kmeans = kmeans.fit_predict(X)

plt.scatter(X.iloc[:,0], X.iloc[:,1], c=y_kmeans)
plt.scatter(kmeans.cluster_centers_[:,0],
            kmeans.cluster_centers_[:,1],
            s=200, marker='X')
plt.title("Customer Segmentation using K-Means")
plt.xlabel("Annual Income")
plt.ylabel("Spending Score")
plt.show()
```

## Output:

![Screenshot_21-2-2026_223153_localhost](https://github.com/user-attachments/assets/3b69cb7d-5aee-44da-a3da-c14128dfee40)

![Screenshot_21-2-2026_223213_localhost](https://github.com/user-attachments/assets/38f752a6-00cc-474d-b055-58a2cf900a8b)

## Result:

Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
