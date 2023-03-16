---
title: What is the process of tracking the route in a breadth-first search?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: Create a dictionary for each node visited, mapping it to its parent node, in order to trace the path in reverse once the target node is found.
---

**Contents**

[TOC]

## Introduction
Breadth-First Search (BFS) is an algorithm used for traversing or searching a graph or tree by exploring all the nodes at the present level before moving on to the next level. In this approach, nodes of a particular level are visited first, and then we move down to the next level. It follows the First-In-First-Out (FIFO) principle for processing nodes. Here are the steps to trace the path in a Breadth-First Search algorithm in Python.

## Section 1: Implement the BFS Algorithm
Before tracing the path, we need to implement the BFS algorithm first. Here are the steps to create a Breadth-First Search algorithm.

1. Create an empty queue and insert the starting node.
2. Create a set to keep track of visited nodes.
3. Run a loop until the queue is not empty.
4. Pop the first element from the queue and add it to the visited set.
5. Check if the popped node is the target node. If yes, return the path.
6. If not, add all the unvisited neighboring nodes to the queue, along with their path.
7. Repeat steps 4 to 7 until the queue is empty.

## Section 2: Keep Track of the Path
To trace the path in a Breadth-First Search algorithm, we need to keep track of the path at each level. Here are the steps to keep track of the path:

1. Create a dictionary to store the path taken to reach each node.
2. When adding a node to the queue, add its path to the dictionary as well.
3. Whenever we visit a node, check if it is the target node. If yes, return the path.
4. If not, add all its unvisited neighboring nodes along with their path to the queue and the dictionary.
5. Repeat steps 3 to 4 until the target node is found.

## Section 3: Return the Path
After the BFS algorithm completes, we can return the path taken to reach the target node. Here are the steps to return the path:

1. Start from the target node and move backwards.
2. Use the dictionary created in section 2 to find the parent of the current node.
3. Append the parent node to the path list.
4. Set the parent node as the current node and repeat steps 2 to 3 until we reach the starting node.
5. Reverse the path list to get the correct order.

## Conclusion
Tracing the path in a Breadth-First Search algorithm is fairly simple. By keeping track of the path at each level and using a dictionary to store the parent of each node, we can easily trace the path from the target node to the starting node.
