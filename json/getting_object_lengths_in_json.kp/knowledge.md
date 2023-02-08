---
title: What is the length of an object?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Use the Object.keys() method to get the length of an object in JSON.
---

**Contents**

[TOC]

1. Retrieve JSON Data 

2. Access JSON Object 

3. Calculate Object Length 

4. Output Object Length 

#### 1. Retrieve JSON Data 

To get the object length of a JSON data, the data must first be retrieved. This can be done by using an AJAX request (for example, using jQuery) to make a call to a server and retrieve the data, or by using a library such as JSON.parse() to parse a JSON string.

#### 2. Access JSON Object 

Once the JSON data has been retrieved, the object can be accessed by using the dot notation or bracket notation. For example, if the JSON data is stored in a variable called `data`, the object can be accessed by using `data.objectName`.

#### 3. Calculate Object Length 

Once the object is accessed, the length of the object can be calculated by using the `Object.keys()` method. This method will return an array of the object's keys, which can then be used to calculate the length of the object.

#### 4. Output Object Length 

Finally, the object length can be outputted by using the `console.log()` method. This will print the object length to the console, which can then be used for further processing.
