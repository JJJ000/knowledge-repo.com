---
title: One possible rephrased version could be "what is the process for extracting decision rules from a decision tree using scikit-learn?"
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the `export\_text` function from `sklearn.tree` to extract the decision rules from a scikit-learn decision-tree in Python.
---

**Contents**

[TOC]

## Introduction

Scikit-learn is a popular Python library for machine learning tasks. One of its most useful functionalities is building Decision Trees. Decision Trees are a powerful tool that can be used for classification and regression tasks. While the trees themselves are useful, it can be even more beneficial to extract the decision rules directly. This tutorial will show you how to extract decision rules from a Scikit-learn decision tree in Python.

## Prerequisites

Before we begin, you should have a basic knowledge of decision trees and Scikit-learn in Python. You should also have Scikit-learn installed on your computer. If you don't have Scikit-learn installed, you can install it using pip in your terminal:

```
pip install scikit-learn
```

## Creating a Decision Tree and Extracting Rules

The first step is to create a decision tree using Scikit-learn. To demonstrate this, let's use the famous Iris dataset. 

``` python
from sklearn.datasets import load_iris
from sklearn.tree import DecisionTreeClassifier

# Load Iris dataset
iris = load_iris()

# Create decision tree
clf = DecisionTreeClassifier()
clf.fit(iris.data, iris.target)
``` 

Once we have created a decision tree, we can use the `export_text` method to extract decision rules. 

``` python
from sklearn.tree import export_text

# Extract decision rules 
tree_rules = export_text(clf, feature_names=iris['feature_names'])
print(tree_rules)
```

The output for the `export_text` method will look like this:

```
|--- petal length (cm) <= 2.45
|   |--- class: 0
|--- petal length (cm) >  2.45
|   |--- petal width (cm) <= 1.75
|   |   |--- petal length (cm) <= 4.95
|   |   |   |--- class: 1
|   |   |--- petal length (cm) >  4.95
|   |   |   |--- sepal width (cm) <= 3.10
|   |   |   |   |--- class: 2
|   |   |   |--- sepal width (cm) >  3.10
|   |   |   |   |--- class: 1
|   |--- petal width (cm) >  1.75
|   |   |--- petal length (cm) <= 4.85
|   |   |   |--- sepal width (cm) <= 3.10
|   |   |   |   |--- class: 2
|   |   |   |--- sepal width (cm) >  3.10
|   |   |   |   |--- class: 1
|   |   |--- petal length (cm) >  4.85
|   |   |   |--- petal width (cm) <= 1.95
|   |   |   |   |--- class: 2
|   |   |   |--- petal width (cm) >  1.95
|   |   |   |   |--- class: 2
```

In the output, each line of rule represents a path from the root of the tree to a leaf node. The first portion of each line represents the condition that needs to be met to follow that path. The second portion of each line shows the predicted class for that path.

## Using Graphviz to Visualize Decision Trees

In addition to the decision rules, it can also be helpful to visualize the decision tree. To do this, we can use Graphviz. If you don't have Graphviz installed, you can install it using pip in your terminal:

```
pip install graphviz
```

Here's an example of how to use Graphviz to visualize the decision tree we created earlier:

``` python
from sklearn.tree import export_graphviz
from IPython.display import Image
import graphviz

# Export decision tree to DOT format
dot_data = export_graphviz(clf, out_file=None, 
                           feature_names=iris.feature_names,  
                           class_names=iris.target_names,  
                           filled=True, rounded=True,  
                           special_characters=True)

# Visualize decision tree
graph = graphviz.Source(dot_data)
graph
```

The output should look something like this:

![Decision Tree Visualization with Graphviz](https://i.imgur.com/kZgX9Oa.png)

## Conclusion

In this tutorial, we learned how to extract decision rules from a Scikit-learn decision tree in Python. We also learned how to use Graphviz to visualize the decision tree. Being able to extract decision rules and visualize decision trees can be incredibly useful for understanding and explaining machine learning models.
