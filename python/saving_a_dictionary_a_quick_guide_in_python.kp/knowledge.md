---
title: What are the steps for saving a dictionary to a file?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the `pickle` module to save the dictionary to a file using `pickle.dump(dictionary, file)` function.
---

**Contents**

[TOC]

## Introduction
In Python, you can use the built-in module 'json' to save a dictionary to a file. The module provides a method 'dump' which takes as input the dictionary and the file object to which you want to save the dictionary. 

## Steps to save a dictionary to a file in Python

### Step 1: Import the json module 
To use the 'dump' method to save a dictionary to a file, you need to import the 'json' module in your Python program. 

```python
import json 
```

### Step 2: Create a dictionary 
Create the dictionary that you want to save to a file. 

```python
dict_example = {'key1': 'value1', 'key2': 'value2'} 
```

### Step 3: Save the dictionary to a file 
Open a file using the 'open' function and specify the mode as 'w' to write to the file. Use the 'dump' method to save the dictionary to the file. 

```python
with open('example_file.json', 'w') as file:
    json.dump(dict_example, file)
``` 

The above code will create a file 'example_file.json' in the current working directory and save the contents of the dictionary 'dict_example' to it. 

### Step 4: Verify the saved dictionary 
You can read the content of the file to verify that the dictionary was saved correctly. 

```python
with open('example_file.json') as file:
    file_content = json.load(file)
    print(file_content)
``` 

The output of the above code should be the contents of the dictionary 'dict_example'. 

## Conclusion 
These are the steps to save a dictionary to a file in Python using the 'json' module. You can use this approach to save any dictionary object to a file in Python.
