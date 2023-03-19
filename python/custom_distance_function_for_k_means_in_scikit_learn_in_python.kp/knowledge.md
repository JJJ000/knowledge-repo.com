---
title: Can one define a custom distance metric for k-means clustering in scikit-learn?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Yes, it is possible to specify your own distance function using scikit-learn K-Means Clustering in Python by creating a custom metric function and passing it to the algorithm.
---

**Contents**

[TOC]

Yes, it is possible to specify your own distance function using scikit-learn K-Means Clustering in Python. Below are the steps you can follow to do this:

### 1. Create a Custom Distance Function
To create a custom distance function, you can define a Python function that takes two vectors (representing two data points) as inputs and returns the distance between them. For instance, let's say you want to use the Euclidean distance as your distance function. You can define the following function:

```python
import numpy as np

def euclidean_distance(x1, x2):
    return np.sqrt(np.sum((x1 - x2)**2))
```

### 2. Create a Custom KMeans Object
Next, you need to create a custom `KMeans` object that uses your custom distance function instead of the default Euclidean distance. You can do this by subclassing `KMeans` and overriding the `pairwise_distances` method as follows:

```python
from sklearn.cluster import KMeans

class CustomKMeans(KMeans):
    def __init__(self, n_clusters=8, max_iter=300, distance_func=euclidean_distance, **kwargs):
        self.distance_func = distance_func
        super().__init__(n_clusters=n_clusters, max_iter=max_iter, **kwargs)

    def pairwise_distances(self, X, Y):
        return np.array([[self.distance_func(x1, x2) for x2 in Y] for x1 in X])
```

In the `__init__` method, we accept an additional parameter `distance_func`, which is set to the default `euclidean_distance` if no custom function is specified. In the `pairwise_distances` method, we calculate the distance matrix using our custom distance function instead of the default implementation.


### 3. Use the Custom KMeans Object
Finally, you can use your custom `CustomKMeans` object to cluster your data. You can pass your custom distance function as a parameter when creating the object, as follows:

```python
data = np.array([[0, 1], [2, 3], [4, 5], [6, 7]])
kmeans_custom = CustomKMeans(n_clusters=2, distance_func=euclidean_distance)
kmeans_custom.fit(data)
```

In this example, we create a `CustomKMeans` object with `distance_func` set to `euclidean_distance` and use it to cluster a small dataset.

### 4. Conclusion
In conclusion, using the steps above, it is possible to specify your own distance function using scikit-learn K-Means Clustering in Python. By subclassing `KMeans` and overriding the `pairwise_distances` method, you can use your custom distance function instead of the default Euclidean distance.
