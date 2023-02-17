---
title: Create a JSON response from a list of objects using flask's jsonify method
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: Flask can jsonify a list of objects by using jsonify() and passing in the list of objects as an argument.
---

**Contents**

[TOC]

#### Creating the List of Objects
To begin, you need to create a list of objects. This can be done in a variety of ways, such as manually creating the objects, or using a library such as Pandas to read in a CSV file. 

#### Flask jsonify
Once you have your list of objects, you can use the Flask jsonify function to convert the list of objects into a JSON response. The jsonify function takes the list of objects as an argument and returns a JSON response.

#### Example
Below is an example of how to use the Flask jsonify function to convert a list of objects into a JSON response.

```
import flask

# Create a list of objects
my_list = [{"name":"John", "age":30}, {"name":"Jane", "age":25}]

# Use the Flask jsonify function to convert the list of objects into a JSON response
response = flask.jsonify(my_list)
```

#### Output
The output of this code will be a JSON response containing the list of objects.

```
[
    {
        "name": "John",
        "age": 30
    },
    {
        "name": "Jane",
        "age": 25
    }
]
```
