---
title: Retrieve JSON data from the jquery.ajax success response
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: The data can be parsed using the JSON.parse() method.
---

**Contents**

[TOC]

# Section 1: Accessing the Data

The JSON data returned from a jQuery.ajax call can be accessed through the `data` argument of the `success` function. This argument contains the response data in string format, so it must be parsed into a JSON object before it can be used.

# Section 2: Parsing the Data

The JSON data can be parsed using the `JSON.parse()` method. This method takes a string as an argument and returns a JavaScript object.

# Section 3: Using the Data

Once the JSON data is parsed, it can be used in the same way as any other JavaScript object. This means that the data can be accessed using `dot` notation, `bracket` notation, or any other method available to JavaScript objects.

# Section 4: Example

For example, if the JSON data returned from the AJAX call is:

```
{
    "name": "John Doe",
    "age": 30
}
```

Then the data can be accessed using the following code:

```
$.ajax({
    url: "example.com",
    success: function(data) {
        var jsonData = JSON.parse(data);
        var name = jsonData.name;
        var age = jsonData.age;
    }
});
```
