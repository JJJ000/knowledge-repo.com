---
title: Output a div containing the pretty-printed version of a JSON string
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: You can use the `prettify` function from JSONFormatter.js to output a JSON string to a div in a pretty print way.
---

**Contents**

[TOC]

## Section 1: Using JSON.stringify 

JSON.stringify() is a built-in function in JavaScript that converts an object or value to a JSON string. This can be used to output a JSON string to a div in a pretty print way.

## Section 2: Syntax 

The syntax for using JSON.stringify is as follows:

```
JSON.stringify(value[, replacer[, space]])
```

where the value is the object or value to be converted to a JSON string, the replacer is an optional parameter that can be used to transform or filter the output, and the space parameter is used to add whitespace to the output string.

## Section 3: Example

For example, the following code will output a JSON string to a div in a pretty print way:

```
var obj = {name: "John", age: 30};

var jsonString = JSON.stringify(obj, null, 4);

document.getElementById("div").innerHTML = jsonString;
```

The output of the above code will be:

```
{
    "name": "John",
    "age": 30
}
```

## Section 4: Conclusion

In conclusion, JSON.stringify can be used to output a JSON string to a div in a pretty print way. The syntax for using JSON.stringify is as follows: JSON.stringify(value[, replacer[, space]]), where the replacer and space parameters are optional. An example of how to use JSON.stringify to output a JSON string to a div in a pretty print way is given above.
