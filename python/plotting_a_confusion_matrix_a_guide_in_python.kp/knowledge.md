---
title: What are the steps to create a confusion matrix?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the scikit-learn library`s confusion\_matrix function and a visualization library such as seaborn or matplotlib to plot a confusion matrix in Python.
---

**Contents**

[TOC]

# Introduction
When working with classification problems, it is important to evaluate the performance of a model. One way to do that is by using a confusion matrix. In this tutorial, we will learn how to plot a confusion matrix in Python.

# Libraries
We will use the following libraries for this tutorial:
- matplotlib: to create the plot
- scikit-learn: to calculate the confusion matrix

# Calculating the Confusion Matrix
To calculate the confusion matrix, we need to have two arrays: the actual values and the predicted values. We can use the `confusion_matrix` function from scikit-learn to calculate it for us. Here's an example:

``` python
from sklearn.metrics import confusion_matrix

actual = [0, 1, 0, 1, 0, 1, 0, 1]
predicted = [1, 1, 0, 1, 0, 0, 0, 1]

cm = confusion_matrix(actual, predicted)
print(cm)
```

Output:
```
array([[2, 2],
       [1, 3]], dtype=int64)
```

# Plotting the Confusion Matrix
Now that we have our confusion matrix, we can plot it using matplotlib. We can use the `imshow` function to display the matrix as an image, and add the values as text using the `text` function. Here's an example:

``` python
import matplotlib.pyplot as plt
import numpy as np

# Define the confusion matrix
cm = np.array([[2, 2], [1, 3]])

# Define the x and y axis labels
labels = ['True Neg', 'False Pos', 'False Neg', 'True Pos']

# Reshape the confusion matrix
cm = cm.reshape((2, 2))

# Plot the confusion matrix as an image
plt.imshow(cm, cmap=plt.cm.Blues)

# Add the values as text
for i in range(2):
    for j in range(2):
        plt.text(j, i, str(cm[i][j]), horizontalalignment='center', color='white')

# Add x and y axis labels
plt.xticks([0, 1], labels[:2])
plt.yticks([0, 1], labels[2:])

# Show the plot
plt.show()
```

Output:
![Confusion Matrix Plot](https://i.imgur.com/dejHwJz.png)

# Conclusion
In this tutorial, we learned how to plot a confusion matrix in Python using scikit-learn and matplotlib. The confusion matrix is a useful tool for evaluating the performance of a classification model, and plotting it can help us better understand the results.
