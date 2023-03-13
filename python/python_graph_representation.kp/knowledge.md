---
title: Expressing the data structure of graphs in the programming language of python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Graphs can be represented in Python using dictionaries to map nodes to their respective neighbors.
---

**Contents**

[TOC]

## Section 1: Introduction

In computer science, graphs are used to represent networks of various kinds, such as social networks, transportation networks, or computer networks. The data structure used to represent graphs in Python can vary depending on the specific needs of the application. In this article, we will explore some of the most common ways to represent graphs in Python.

## Section 2: Adjacency Matrix

One common way to represent a graph in Python is to use an adjacency matrix. An adjacency matrix is a rectangular matrix where each row and column corresponds to a vertex in the graph. The value in each position of the matrix corresponds to the weight of the edge between the vertices represented by the row and column.

```python
# Creating an adjacency matrix in Python
graph = [[0, 1, 0, 0],
         [1, 0, 1, 1],
         [0, 1, 0, 1],
         [0, 1, 1, 0]]
```

## Section 3: Adjacency List

Another way to represent a graph in Python is to use an adjacency list. An adjacency list is a dictionary where the keys are the vertices in the graph and the values are lists of vertices that the key vertex is connected to.

```python
# Creating an adjacency list in Python
graph = {0: [1],
         1: [0, 2, 3],
         2: [1, 3],
         3: [1, 2]}
```

## Section 4: NetworkX

Finally, for more complex graph applications, Python programmers might choose to use the NetworkX library. NetworkX provides an API that allows developers to create, manipulate, and analyze complex graphs with many vertices and edges.

```python
# Creating a graph with NetworkX
import networkx as nx

G = nx.Graph()
G.add_node(1)
G.add_node(2)
G.add_edge(1, 2)
```

## Conclusion

There are many ways to represent graphs in Python, from simple adjacency matrices and lists to more powerful libraries like NetworkX. The choice of data structure depends on the complexity of the graph and the specific needs of the application.
