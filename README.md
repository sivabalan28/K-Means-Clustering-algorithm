# Implementation of K-Means Clustering Algorithm
## Aim
To write a python program to implement K-Means Clustering Algorithm.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation

## Algorithm:

### Step1
import pandas,matplotlib,sklearn,lseaborn,warnings

### Step2
read the csv file

### Step3
print the first five data of csv file

### Step4
use scatterplot and plot income for x and loan for y and plot the graph

### Step5
use kmean ,kmean fit

### Step6
print the output

## Program:
```python

import pandas as pd
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans
import seaborn as sns
import warnings
warnings.filterwarnings('ignore')

data=pd.read_csv("clustering.csv")
print(data.head(5))

x1=data.loc[:,['ApplicantIncome','LoanAmount']]
print(x1.head(2))

x=x1.values
sns.scatterplot(x[:,0],x[:,1])
plt.xlabel('Income')
plt.ylabel('Loan')
plt.show()

Kmean=KMeans(n_clusters=4)
Kmean.fit(x)

print("cluster centers:",Kmean.cluster_centers_)
print("labels:",Kmean.labels_)

predicted_cluster=Kmean.predict([[9200,110]])
print("the cluster group for the applicantincome 9200 and loan amount 110 is",predicted_cluster)

```
## Output:

![output](/koutput1.png)

<br>

## Result
Thus the K-means clustering algorithm is implemented and predicted the cluster class using python program.