---
title: What is the syntax for saving a JavaScript function in json?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: You can store a JavaScript function in JSON by stringifying it.
---

**Contents**

[TOC]

1. Syntax for Storing a JavaScript Function in JSON
-----------------------------------------------
A JavaScript function can be stored in JSON by using the following syntax:

```
{
  "myFunction": "function(param1, param2) {
    // Function code here
  }"
}
```

2. Example of Storing a JavaScript Function in JSON
--------------------------------------------------
The following is an example of a JavaScript function stored in JSON:

```
{
  "myFunction": "function(name) {
    console.log('Hello ' + name);
  }"
}
```

3. Accessing the JavaScript Function
-----------------------------------
The stored JavaScript function can be accessed by using the following syntax:

```
var myFunction = JSON.parse(jsonObject).myFunction;
myFunction('John'); // Outputs 'Hello John'
```

4. Executing the JavaScript Function
-----------------------------------
The stored JavaScript function can be executed by using the following syntax:

```
eval(JSON.parse(jsonObject).myFunction)('John'); // Outputs 'Hello John'
```
