---
title: Print JSON in a readable format using python's built-in JSON library
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the json.dumps() function with the indent parameter set to a desired number of spaces.
---

**Contents**

[TOC]

# Section 1: Using the json Module
The json module is a built-in module in Python that allows us to work with JSON data. To pretty-print a JSON object in Python, we can use the json.dumps() method. This method takes an object as an argument and returns a string that is formatted as a JSON object.

# Section 2: Specifying the Indentation
The json.dumps() method has an optional parameter called indent. This parameter specifies the indentation of the JSON object. By default, the indentation is set to None, which means that the JSON object will be printed on a single line. If we set the indent parameter to a positive integer, the JSON object will be printed with that many spaces for indentation.

# Section 3: Setting the Sort Keys
Another optional parameter of the json.dumps() method is sort_keys. This parameter is a boolean value that specifies whether the keys in the JSON object should be sorted or not. By default, the sort_keys parameter is set to False, which means that the keys are not sorted. If we set the sort_keys parameter to True, the keys in the JSON object will be sorted in alphabetical order.

# Section 4: Outputting to a File
The json.dumps() method can also be used to output the JSON object to a file. To do this, we can open a file in write mode and pass the file object to the json.dumps() method as an argument. The JSON object will be written to the file.
