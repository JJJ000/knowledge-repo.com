---
title: What is the syntax for creating a JSON object using jquery?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: jQuery can create JSON objects using the $.parseJSON() method.
---

**Contents**

[TOC]

1. Creating JSON Object in jQuery
---------------------------------

JSON objects can be created in jQuery using the `$.extend()` method. This method takes two or more objects and merges them together into a single object.

2. Syntax
---------

The syntax for creating a JSON object in jQuery looks like this:

```javascript
var jsonObject = $.extend( {}, object1, object2, ... );
```

3. Example
----------

Here is an example of creating a JSON object in jQuery:

```javascript
var jsonObject = $.extend( {}, 
    { 
        "name": "John Doe", 
        "age": 25 
    }, 
    { 
        "city": "New York", 
        "country": "USA" 
    } 
);
```

4. Output
---------

The output of the above code is a JSON object that looks like this:

```json
{
    "name": "John Doe",
    "age": 25,
    "city": "New York",
    "country": "USA"
}
```
