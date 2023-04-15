---
title: A class in Python that mimics the functionality of a dictionary
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The `collections` module in Python provides a class called `UserDict` that acts like a dictionary.
---

**Contents**

[TOC]

# Introduction

In this task, we have to implement a Python class that acts like a dictionary. Python provides built-in dict() function for creating a dictionary, but if we want to implement a class similar to this with some additional functionalities. 

# Creating a class

We can start by defining a Python class named ‘CustomDict’ that mimics the dict() function. The class should have the same functionalities as are in the built-in dict() function. 

```python
class CustomDict:
    def __init__(self, **kwargs):
        self.data = {}
        for key, value in kwargs.items():
            self.data[key] = value

    def __getitem__(self, key):
        return self.data[key]

    def __setitem__(self, key, value):
        self.data[key] = value

    def __delitem__(self, key):
        del self.data[key]

    def __iter__(self):
        return iter(self.data)

    def __len__(self):
        return len(self.data)
```

The above class has following functionalities,

* `__init__` – We are initializing a dictionary data with the values passed through **kwargs.

* `__getitem__` – This method is used for accessing the value of a particular key. If the key is not found, it will raise KeyError.

* `__setitem__` – This method is used for setting the value to a key.

* `__delitem__` – This method is used for deleting the item with a particular key passed.

* `__iter__` – This is used to iterate over all the keys present in the dictionary.

* `__len__` – This is used to return the number of key-value pairs present in the dictionary.  

# Usage

Now we can create an object of class CustomDict and use it.

```python
d = CustomDict(a=1, b=2, c=3)

print(d['a'])
d['b'] = 4

for key in d:
    print(key, d[key])

del d['c']
print(len(d))
```

Output
```
1
a 1
b 4
3
```

We can see that the above class is working with functionalities similar to the built-in dict() function. 

# Conclusion

In this task, we have implemented a Python class similar to the dict() function. We have seen that using this class, we can have additional functionalities according to our requirements.
