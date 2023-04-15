---
title: The hash function in Python 3.3 gives dissimilar outcomes in separate sessions
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Due to the randomization of the hash seed on each new Python session, hash function in Python 3.3 returns different results between sessions.
---

**Contents**

[TOC]

Introduction

Hash functions are essential tools in computer science that help us store and retrieve information faster. A hash function maps an input data of an arbitrary length to an output data of a fixed length. Python 3.3 provides hash functions that are used to implement dictionaries and other containers. In this essay, I will discuss an issue in Python 3.3 hash function where the returned results vary between sessions. 

Python's hash function 

Python's hash function takes an object as input and returns a hash value that represents the object. Hash values are integers that are unique for each object instance and matches for two equal objects. For example, two strings 'hello' and 'hello' will have the same hash value. The hash function is used extensively to implement dictionaries, sets, and frozen sets in Python.  

hash function returns different output between sessions 

One of the issues with the hash function in Python 3.3 is that it returns different results between sessions for the same input object. This issue has been reported by several developers in various forums, including StackOverflow. This behavior is unintentional and affects the performance of applications that depend on the hash function. 

Possible reasons for the issue 

There are several possible reasons why the hash function in Python 3.3 returns different results between sessions. One reason could be the use of the hash randomization feature in the interpreter. When hash randomization is enabled, a random seed is added to the hash value to prevent denial of service attacks that use hash collisions. This feature was introduced in Python 3.3, and it's enabled by default. 

Another reason could be the changes in the hash algorithm used to compute the hash value. Python 3.3 introduced a new hash algorithm that is faster than the previous one used in Python 2.x. However, this algorithm may also produce a different output for the same input object. 

Conclusion

In conclusion, Python 3.3 hash function returns different results between sessions due to hash randomization and changes in the hash algorithm. This behavior affects the performance of applications that rely on the hash function, and developers should take it into account when developing their applications. One solution to this issue is to disable hash randomization by setting the PYTHONHASHSEED environment variable to a fixed value. Alternatively, developers can use alternative hash functions that are not affected by this issue.
