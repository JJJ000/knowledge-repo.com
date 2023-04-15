---
title: Utilizing pickle to store and retrieve objects
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Pickle is a Python module that allows you to save and load objects from files, making it easy to store and retrieve data in a reusable format.
---

**Contents**

[TOC]

# Introduction
In Python, we often need to save certain objects such as dictionaries, lists, arrays, or any other data that we have generated during the execution of our code. This can be done using the `pickle` module which is a built-in Python module that can serialize and de-serialize objects so that they can be stored and retrieved from a file or memory. In this tutorial, we will learn how to use the `pickle` module to save and load objects in Python.


# Saving Objects using pickle
To save an object using `pickle`, we first need to import the module. After that, we can use the `pickle.dump()` function to save the object to a file. The function takes two arguments:

1. The object we want to save
2. The name of the file we want to save it to


```python
import pickle

# object to serialize
my_object = {'name': 'John', 'age': 25, 'hobbies': ['reading', 'gaming', 'coding']}

# open the file in write mode
with open('object.pickle', 'wb') as file:
    # use pickle.dump() to save the object
    pickle.dump(my_object, file)
```


# Loading Objects using pickle
To load an object using `pickle`, we can use the `pickle.load()` function. This function takes a single argument which is the file we want to read from.


```python
import pickle

# open the file in read mode
with open('object.pickle', 'rb') as file:
    # use pickle.load() to load the object
    loaded_object = pickle.load(file)
    
print(loaded_object)
```


# Saving and Loading Multiple Objects
We can also save and load multiple objects using `pickle`. To do this, we need to pass a tuple of the objects we want to save to the `pickle.dump()` function. Similarly, we need to read the objects one by one using `pickle.load()` function.


```python
import pickle

# objects to serialize
obj1 = {'name': 'John', 'age': 25, 'hobbies': ['reading', 'gaming', 'coding']}
obj2 = [1, 2, 3, 4, 5]

# open the file in write mode
with open('objects.pickle', 'wb') as file:
    # use pickle.dump() to serialize the objects
    pickle.dump((obj1, obj2), file)

# open the file in read mode
with open('objects.pickle', 'rb') as file:
    # use pickle.load() to deserialize the objects
    loaded_obj1, loaded_obj2 = pickle.load(file)

print(loaded_obj1)
print(loaded_obj2)
```


# Conclusion
In this tutorial, we learned how to use the `pickle` module in Python to save and load objects. We saw how to save an object to a file using `pickle.dump()` and how to load an object from a file using `pickle.load()`. Finally, we saw how to save and load multiple objects using `pickle`.
