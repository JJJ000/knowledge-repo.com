---
title: Transform a string object into a JSON object
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: The object string can be converted to JSON by using the JSON.parse() method.
---

**Contents**

[TOC]

# Section 1: Parse Object String

To parse an object string into JSON, you can use the JSON.parse() method. This method takes a string as an argument and returns a JavaScript object or array.

# Section 2: Syntax

The syntax for the JSON.parse() method is as follows:

```
JSON.parse(string)
```

# Section 3: Example

For example, if you have a string that represents an object like this:

```
"{ "name": "John", "age": 30 }"
```

You can parse it into a JavaScript object like this:

```
var obj = JSON.parse("{ "name": "John", "age": 30 }");
```

# Section 4: Output

The output of the above code will be a JavaScript object with the properties "name" and "age".
