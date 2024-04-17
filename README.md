# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: Gokkul M
RegisterNumber: 212223240039
import pandas as pd
from sklearn.cluster import KMeans
import matplotlib.pyplot as plt
df=pd.read_csv("Mall_Customers.csv")
print(df.head())
print(df.info())
print(df.isnull().sum())
wcss=[]
for i in range(1,11):
    kmeans=KMeans(n_clusters=i,init="k-means++")
    kmeans.fit(df.iloc[:,3:])
    wcss.append(kmeans.inertia_)
plt.plot(range(1,11),wcss)
plt.xlabel("No.of Clusters")
plt.ylabel("wcss")
plt.title("Elbow Method")
km=KMeans(n_clusters=5)
km.fit(df.iloc[:,3:])
y_pred=km.predict(df.iloc[:,3:])
print(y_pred)
df["cluster"]=y_pred
df0=df[df["cluster"]==0]
df1=df[df["cluster"]==1]
df2=df[df["cluster"]==2]
df3=df[df["cluster"]==3]
df4=df[df["cluster"]==4]
plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster0")
plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="black",label="cluster1")
plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="blue",label="cluster2")
plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="green",label="cluster3")
plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="yellow",label="cluster4")
print(plt.legend())
print(plt.title("Customer Segment"))
```
## Output:
![image](https://github.com/Gokkul-M/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/144870543/4783cad0-2460-4a4b-90e1-b33600eb0fec)
## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
