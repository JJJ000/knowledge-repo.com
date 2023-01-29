---
title: Starting number of elements for the arraylist
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The initial size of an ArrayList in Java is 10.
---

**Contents**

[TOC]

1. Default Size
    By default, the size of an ArrayList in Java is 0.

2. Initialization
    An ArrayList can be initialized with a certain size by using the following syntax:
    ```java
    ArrayList<Type> list = new ArrayList<>(initialSize);
    ```

3. Capacity
    The capacity of an ArrayList is the number of elements that can be stored in the list without having to increase its size.

4. Expansion
    When the ArrayList reaches its capacity, its size is automatically increased by 50%.
