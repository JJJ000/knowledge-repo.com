---
title: What is the last element of an arraylist?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The last value of an ArrayList in Java can be accessed using the list`s size()-1 index.
---

**Contents**

[TOC]

### Accessing the Last Value

The simplest way to access the last value of an ArrayList in Java is to use the `get()` method. This method takes an index as an argument, and returns the element at that index in the ArrayList. To access the last element, we simply need to pass the ArrayList's size minus one as the index.

### Example Code

Below is an example of how to access the last element of an ArrayList in Java:

```java
ArrayList<String> list = new ArrayList<>();
list.add("foo");
list.add("bar");
list.add("baz");

String lastElement = list.get(list.size() - 1); // lastElement == "baz"
```

### Performance Considerations

It is important to note that using the `get()` method to access the last element of an ArrayList is not the most efficient approach. This is because the `get()` method must iterate through the entire list to find the requested element, which can be a time-consuming operation for large lists.

### Alternative Approaches

If performance is an issue, a better approach would be to use the `remove()` method to remove the last element from the list and return it. This approach avoids the need to iterate through the entire list, and can be significantly faster in certain cases.
