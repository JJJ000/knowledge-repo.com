---
title: How can I distribute a dictionary among various processes while using multiprocessing?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: Use a multiprocessing Manager to create a shared dictionary that can be accessed and modified by multiple processes.
---

**Contents**

[TOC]

# Introduction

In multiprocessing, sharing data among different processes is challenging due to the fact that they do not share memory space. Therefore, it is necessary to implement ways to share data between these processes. One of the most straightforward ways of sharing data among multiple processes is by using managers. In this tutorial, you will learn how to share a dictionary among multiple processes in Python using the multiprocessing module.

# Creating a Shared Dictionary

To create a shared dictionary, we need to use the multiprocessing Manager class. This class creates a server process that holds Python objects and allows other processes to interact with them. The Manager class provides a way to create a shared dictionary, which can be accessed by multiple processes.

```python
from multiprocessing import Manager

manager = Manager()
d = manager.dict()
```

The `Manager` class from the `multiprocessing` module is used to create a shared memory space where objects can be shared between processes. This class provides a method called `dict()` which creates a shared dictionary object.

# Accessing and modifying the Shared Dictionary

Once a shared dictionary is created, we can access and modify it by different processes. 

```python
from multiprocessing import Process, Manager

def modify_dict(d, key, value):
    d[key] = value

if __name__ == '__main__':
    manager = Manager()
    d = manager.dict()
    p1 = Process(target=modify_dict, args=(d, 'key1', 'value1'))
    p2 = Process(target=modify_dict, args=(d, 'key2', 'value2'))

    p1.start()
    p2.start()

    p1.join()
    p2.join()

    print(d)
```

In the above example, two processes are created, both of which are using the same shared dictionary. The `modify_dict` function takes a dictionary, a key, and a value as parameters and modifies the dictionary by setting the value for the given key. Here, we are creating two processes `p1` and `p2`, and modifying the dictionary by setting values for 'key1' and 'key2'. Finally, we are printing the modified dictionary. Notice that the final dictionary contains both key-value pairs, showing that both processes are able to modify the shared dictionary.

# Conclusion

In this tutorial, you learned how to share a dictionary among multiple processes in Python using the multiprocessing module. By creating a shared dictionary using the Manager class and accessing and modifying it through different processes, you can easily share data among multiple processes.
