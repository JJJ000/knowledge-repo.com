---
title: Transform array into json
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Use the JSON.stringify() method to convert an array to JSON.
---

**Contents**

[TOC]

# Section 1: Convert Array to JSON

Converting an array to JSON is a simple process. The array must first be defined and then the JSON.stringify() method can be used to convert the array to a JSON string.

# Section 2: Defining an Array

An array can be defined using the following syntax: 

```
let myArray = [1,2,3,4,5];
```

# Section 3: Using JSON.stringify()

Once the array has been defined, the JSON.stringify() method can be used to convert the array to a JSON string. This method takes the array as an argument and returns a JSON string.

```
let myJSONString = JSON.stringify(myArray);
```

# Section 4: Output

The output of the JSON.stringify() method will be a JSON string in the following format:

```
"[1,2,3,4,5]"
```
