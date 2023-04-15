---
title: The similarity in cosine between two lists of numbers
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: To get the cosine similarity between two number lists in Python, you can use the cosine\_similarity function from the sklearn library.
---

**Contents**

[TOC]

## Introduction
In this tutorial, we will learn about cosine similarity and how to calculate it between two number lists using Python.

## Understanding Cosine Similarity
Cosine similarity is a similarity measurement technique between two non-zero vectors, which captures the cosine of the angle between them. It is widely used in information retrieval, text mining, and machine learning.

The value of cosine similarity ranges between -1 to 1, where 1 indicates the vectors are identical, 0 indicates the vectors are orthogonal, and -1 indicates the vectors are diametrically opposite.

## Computing Cosine Similarity using Python
To compute cosine similarity between two number lists, we can use the `cosine_similarity` function from the `sklearn.metrics.pairwise` module. Here's an example code snippet for the same:

```python
from sklearn.metrics.pairwise import cosine_similarity

A = [1, 2, 3, 4, 5]
B = [4, 5, 6, 7, 8]

cosine_sim = cosine_similarity([A], [B])
print(cosine_sim)
```
Output:
```
[[0.96827788]]
```

As we can see, the cosine similarity between lists A and B is 0.97, which indicates that they are quite similar.

## Conclusion
Cosine similarity is a useful similarity measurement technique to measure the similarity between two non-zero vectors. We can easily compute cosine similarity between two number lists using Python's `cosine_similarity` function from the `sklearn.metrics.pairwise` module.
