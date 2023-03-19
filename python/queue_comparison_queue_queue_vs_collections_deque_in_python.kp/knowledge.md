---
title: The difference between queue.queue and collections.deque
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Queue.Queue is a synchronized queue while collections.deque is not synchronized, meaning it cannot be used in a multi-threaded environment without additional locking.
---

**Contents**

[TOC]

# Introduction

The `Queue` module and `collections.deque` module in Python are used to implement queues, which are important data structures used in programming. Although both of them serve the same purpose, that is, to add or remove elements from a queue, there are some differences between them. In this article, we will compare `Queue.Queue` and `collections.deque` in Python and see the advantages and disadvantages of each one.

# Queue.Queue

`Queue.Queue` is a module in Python that provides a queue data structure. It provides a `Queue` class with many methods to add or remove elements from the queue. It is thread-safe and can be used in an environment where multiple threads are accessing the same data structure.

However, some disadvantages of `Queue.Queue` are:

- When using the `Queue` class in Python, you have to specify the maximum size of the queue.
- If the queue has reached its maximum size, adding an element to the queue will result in an error.

# collections.deque

`collections.deque` is another module in Python that provides a queue data structure. It provides a `deque` class with many methods to add or remove elements from a queue. It is not thread-safe and should not be used in an environment where multiple threads are accessing the same data structure.

However, some advantages of `collections.deque` are:

- Unlike `Queue.Queue`, you don't need to specify the maximum size of the queue when using `collections.deque`.
- If the queue has reached its maximum size, adding an element to the queue will remove the first element in the queue to make space for the new element.

# Conclusion

Both `Queue.Queue` and `collections.deque` provide a queue data structure in Python, but they have some differences. If you are working in an environment where multiple threads are accessing the same data structure, `Queue.Queue` is a good option because it is thread safe. However, if you don't want to specify the maximum size of the queue, or if you want to remove the first element in the queue when adding a new element to a full queue, then `collections.deque` is a better option.
