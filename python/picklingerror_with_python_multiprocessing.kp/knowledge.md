---
title: It is not possible to pickle a Python function using the multiprocessing module, which results in a picklingerror
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You cannot pickle functions because they are not serializable.
---

**Contents**

[TOC]

# Introduction

The PicklingError is an error encountered in Python when attempting to serialize an object that cannot be serialized. This error is often encountered when using the multiprocessing module, as the module relies on pickling to serialize objects in order to pass them between processes. In this article, we will discuss the PicklingError encountered when attempting to pickle a function, and how to resolve it.

# Causes of the Error

The PicklingError is caused when an object is attempted to be serialized that cannot be serialized. In the case of functions, this is because functions are not serializable, and thus cannot be pickled. This is because functions are not immutable, meaning that they can be changed at runtime and thus cannot be serialized.

# Solutions

The simplest solution to this problem is to avoid attempting to pickle functions. Instead, pass the function as an argument to the multiprocessing function, and have the function execute in the child process. This will allow the function to be executed without needing to be pickled.

Another solution is to use a library such as dill, which provides a way to pickle functions. This library is designed to allow for the serialization of functions, and thus can be used to pickle functions for use in multiprocessing.

# Conclusion

The PicklingError encountered when attempting to pickle a function is caused by the fact that functions are not serializable. The simplest solution to this problem is to avoid attempting to pickle functions, and instead pass the function as an argument to the multiprocessing function. Alternatively, a library such as dill can be used to allow for the pickling of functions.
