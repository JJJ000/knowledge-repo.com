---
title: What is the process for determining if a string is a valid JSON string?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the JSON.parse() method to check if a string is a valid JSON string.
---

**Contents**

[TOC]

#1 Using the JSON.parse() Method
The JSON.parse() method can be used to check if a string is valid JSON. The method will return an object if the string is valid JSON, and will throw an error if the string is not valid JSON.

#2 Example
Below is an example of using the JSON.parse() method to check if a string is valid JSON.

```
try {
  var jsonString = '{"name":"John", "age":30}';
  var jsonObj = JSON.parse(jsonString);
  console.log("Valid JSON string");
} catch (e) {
  console.log("Invalid JSON string");
}
```

#3 Output
If the string is valid JSON, the output will be:

```
Valid JSON string
```

If the string is invalid JSON, the output will be:

```
Invalid JSON string
```

#4 Conclusion
The JSON.parse() method can be used to check if a string is valid JSON. If the string is valid JSON, the method will return an object. If the string is invalid JSON, the method will throw an error.
