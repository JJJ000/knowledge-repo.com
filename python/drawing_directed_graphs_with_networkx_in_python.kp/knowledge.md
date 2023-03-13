---
title: What is the process for creating directed graphs in Python utilizing networkx?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Use the `add\_edge()` method of the `DiGraph()` class in networkx to create edges with a direction.
---

**Contents**

[TOC]

# Introduction
NetworkX is a Python package used for the creation, manipulation, and study of the structure, dynamic, and functions of complex networks. It provides tools for creating different types of graphs, such as directed and undirected graphs. This tutorial explains how to draw directed graphs using NetworkX in Python.

## Installing NetworkX 
Before we start, we need to install NetworkX using pip. Open a terminal and type the following command:

```python
pip install networkx
```

## Creating a Directed Graph
To create a directed graph, we need to import the `networkx` module and create an instance of `DiGraph()` class.

```python
import networkx as nx

G = nx.DiGraph()
```

## Adding Nodes and Edges
To add nodes and edges to our directed graph, we can use `add_node()` and `add_edge()` methods of the `DiGraph()` class. 

```python
G.add_node(1)
G.add_node(2)
G.add_node(3)

G.add_edge(1, 2)
G.add_edge(2, 3)
```

## Drawing a Directed Graph
To draw a directed graph, we can use the `draw()` function of the `networkx` module. We also need to use the `pyplot` module of `matplotlib` to show the graph on the screen.

```python
import matplotlib.pyplot as plt

nx.draw(G, with_labels=True, node_color='lightblue', edge_color='grey', arrowsize=20, linewidths=1,
        font_size=15, font_weight='bold', node_size=500)

plt.show()
```

This will draw a directed graph on the screen with nodes and edges represented by circles and directed arrows, respectively. 

## Complete Code Example
```python
import networkx as nx
import matplotlib.pyplot as plt

G = nx.DiGraph()

G.add_node(1)
G.add_node(2)
G.add_node(3)

G.add_edge(1, 2)
G.add_edge(2, 3)

nx.draw(G, with_labels=True, node_color='lightblue', edge_color='grey', arrowsize=20, linewidths=1,
        font_size=15, font_weight='bold', node_size=500)

plt.show()
```

This will create and draw a directed graph with three nodes and two edges.
