---
title: How to retrieve an object using its id()?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The id() function in Python returns the unique integer identifier of an object.
---

**Contents**

[TOC]

### Introduction 

In Python, every object that we create is given a unique identifier, which is represented by the `id()` function. These ids are used to distinguish between different objects, even if they have the same value. In this article, we will discuss how to retrieve an object by its id using Python. 

### Assigning an Id to an Object

In Python, every object is assigned a unique identifier when it is created. You can use the `id()` function to get the identifier assigned to an object. For example:

```python
a = 10
print(id(a)) # Output: 4367470352
```

### Retrieving an Object by Its Id

Python does not provide a built-in method for retrieving an object by its id. However, we can use a dictionary to store objects and their ids, and use the id as the key to retrieve the object. Here's an example:

```python
# create an empty dictionary to store objects
objects = {}

# create an object and add it to the dictionary
a = [1, 2, 3]
objects[id(a)] = a

# retrieve the object by its id
b = objects[<id>]
print(b)
```

In the above example, we create a dictionary called `objects` to store objects using their ids as the key. We then create an object `a` and add it to the dictionary with the id as the key. To retrieve the object, we simply need to access it using the id as the key.

### Conclusion

Retrieving an object by its id in Python can be done by storing objects in a dictionary using their ids as the key. This approach provides a way to look up objects by their ids, which can be useful in some situations where you need to reference an object in memory. However, it is important to note that this approach can be memory-intensive, as each object added to the dictionary will remain in memory until it is explicitly removed.
