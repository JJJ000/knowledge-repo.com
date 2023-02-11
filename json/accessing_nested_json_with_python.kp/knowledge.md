---
title: Retrieving nested JSON data using python
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: You can access nested JSON data in JSON by using the dot notation to access the nested data.
---

**Contents**

[TOC]

1. Introduction 

JSON (JavaScript Object Notation) is a lightweight data-interchange format. It is a text-based format that is designed to facilitate the exchange of data between different systems. It is an open standard that is used to store and transport data. JSON is widely used in web applications and mobile apps.

2. Accessing Nested JSON Data 

Nested JSON data is a collection of objects or arrays within an object or array. It is a hierarchical structure that can be used to store and retrieve data. Accessing nested JSON data can be tricky, as it requires traversing the hierarchical structure.

In order to access nested JSON data, you must use dot notation or bracket notation. Dot notation is used to access the properties of an object. Bracket notation is used to access the elements of an array.

3. Examples 

Let’s take a look at an example of nested JSON data.

{
  "name": "John Doe",
  "age": 30,
  "address": {
    "street": "123 Main Street",
    "city": "New York",
    "state": "NY"
  },
  "hobbies": ["reading", "sports", "movies"]
}

To access the address object, you would use dot notation:

var address = data.address;

To access the city property of the address object, you would use dot notation again:

var city = data.address.city;

To access the first element of the hobbies array, you would use bracket notation:

var hobby = data.hobbies[0];

4. Conclusion

In conclusion, accessing nested JSON data can be tricky. It requires the use of dot notation or bracket notation to traverse the hierarchical structure. With the right tools and knowledge, you can easily access and manipulate nested JSON data.
