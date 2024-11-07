# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the necessary packages using import statement.  
2.Read the given csv file using read_csv() method and print the number of contents to be displayed using df.head().  
3. Import KMeans and use for loop to cluster the data.  
4.Predict the cluster and plot data graphs.   
5.Print the outputs and end the program    

## Program:
```

Program to implement the K Means Clustering for Customer Segmentation.
Developed by: ARCHANA T
RegisterNumber: 212223240013 
import pandas as pd
import matplotlib.pyplot as plt
data = pd.read_csv("/content/Mall_Customers.csv")
data.head()
data.info()
data.isnull().sum()from sklearn.cluster import KMeans
wcss = []
for i in range(1,11):
    kmeans = KMeans(n_clusters = i,init = "k-means++")
    kmeans.fit(data.iloc[:,3:])
    wcss.append(kmeans.inertia_)
plt.plot(range(1,11),wcss)
plt.xlabel("No.of Clusters")
plt.ylabel("wcss")
plt.title("Elbow Method")
km=KMeans(n_clusters=5)
km.fit(data.iloc[:,3:])
KMeans(n_clusters=5)
y_pred=km.predict(data.iloc[:,3:])
y_pred
data["cluster"]=y_pred
df0 = data[data["cluster"]==0]
df1 = data[data["cluster"]==1]
df2 = data[data["cluster"]==2]
df3 = data[data["cluster"]==3]
df4 = data[data["cluster"]==4]
plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"], color = "gold")
plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"], color = "pink")
plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"], color = "green")
plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"], color = "blue")
plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"], color = "red")
plt.show()

```

## Output:
![K Means Clustering for Customer Segmentation](sam.png)
![image](https://github.com/user-attachments/assets/85965d39-42ec-4b7b-8e29-980ee7225b44)
![image](https://github.com/user-attachments/assets/9affa825-5349-4268-8766-27503d66e739)
![image](https://github.com/user-attachments/assets/eab71fee-9935-4ba7-8baf-daed3c7e24b6)
![image](https://github.com/user-attachments/assets/07524f87-a516-417c-a271-e20dddbc7e9d)
![image](https://github.com/user-attachments/assets/cd760641-8459-46fd-af7a-287ca996a079)
![image](https://github.com/user-attachments/assets/3e99d60b-7eb3-4e16-94c4-b2040dcb9d0f)




## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
