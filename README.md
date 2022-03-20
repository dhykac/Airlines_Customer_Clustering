# Airlines_Customer_Clustering

This repository is about airlines customer clustering using K Means (unsupervised ML)

* [Dataset](https://github.com/dhykac/Airlines_Customer_Clustering/blob/main/airlines_customers.csv)
* [Notebook](https://github.com/dhykac/Airlines_Customer_Clustering/blob/main/Airlines%20Customer%20Clustering.ipynb)

## Packages
```python
import warnings
warnings.filterwarnings('ignore')

import numpy as np
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
%matplotlib inline

from sklearn.preprocessing import StandardScaler, MinMaxScaler
from sklearn.decomposition import PCA 
from sklearn.cluster import KMeans
```

## Results Overview

![Radar Plot](https://user-images.githubusercontent.com/92696555/159148684-56aa55b8-72c6-43fd-8b70-a2b2b155dc8a.png)

From the [summary](https://github.com/dhykac/Airlines_Customer_Clustering/blob/main/Airlines%20Customer%20Clustering.ipynb) and the visualization above, we know that there are 3 customer cluster :

* Cluster 1 (low-level customers) : It shows this cluster have highest `LAST_TO_END` which means this kind of customers have longest recency than other two. In the term of membership, this customers have shortest `MEMBER_DUR_MONTHS` which means either this customers are new membership or just old member whom churned from the company. Meanwhile, the three other columns have smallest values than others indicate the class and also the segmentation for this cluster. The company need to formulate new marketing strategy in order to increase transaction from this cluster.

* Cluster 2 (middle-level customers) : The Cluster absolutely stand on the middle of the crowds in every columns. This means this kind of customers stand between the low-level and high-level customers with all columns have middle values from all cluster members. The company just need to maintain the customers to encourage them in order raised the transactions

* Cluster 3 (high-level customers) : Now we move to the highest level customers. No doubt that these customers contribute mostly to the company. Loyal customers determine by `MEMBER_DUR_MONTHS` and also high recency by `LAST_TO_END` shows how these customers believe in company. `avg_discount` also show the higher buying power than other two clusters. The company must improve their satisfaction because indeed these customers is main power of the company.
