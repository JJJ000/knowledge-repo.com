---
title: A numpy array cannot be converted into a JSON object
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: No, NumPy arrays are not JSON serializable.
---

**Contents**

[TOC]

#Solution
##1. What is JSON?
JSON (JavaScript Object Notation) is a lightweight data-interchange format. It is a text-based, human-readable format for representing simple data structures and associative arrays (called objects).

##2. Why NumPy Array is Not JSON Serializable?
NumPy arrays are not JSON serializable because the JSON standard only supports the following data types: strings, numbers, booleans, lists, dictionaries, and null. NumPy arrays are not one of these data types and therefore cannot be serialized.

##3. How to Serialize a NumPy Array?
To serialize a NumPy array, you can use the built-in json library. The json library can convert a NumPy array into a JSON string.

##4. What are the Alternatives?
If you want to serialize a NumPy array, you can also use the pickle library or the h5py library. Pickle is a Python library that can serialize any Python object, including NumPy arrays. H5py is a library for working with HDF5 files, which can store NumPy arrays.
