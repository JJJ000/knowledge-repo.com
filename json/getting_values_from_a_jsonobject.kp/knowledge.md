---
title: What is the process of retrieving a value from a jsonobject?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: Use the get() method to retrieve the value associated with a given key in a JSONObject.
---

**Contents**

[TOC]

1. Accessing JSON Values
---------------------------------
JSON values can be accessed using dot notation or bracket notation. 

2. Dot Notation
---------------------------------
Dot notation is the simplest way to access JSON values. It requires the use of the dot operator (.) to access the value associated with a given key.

For example, if we have the following JSON object:

```
{
  "name": "John Doe",
  "age": 30
}
```

We can access the value of the "name" key using dot notation like this: 

```
jsonObject.name
```

3. Bracket Notation
---------------------------------
Bracket notation requires the use of the bracket operator ([]) to access the value associated with a given key.

For example, if we have the same JSON object as before: 

```
{
  "name": "John Doe",
  "age": 30
}
```

We can access the value of the "name" key using bracket notation like this: 

```
jsonObject["name"]
```

4. Conclusion
---------------------------------
In conclusion, JSON values can be accessed using either dot notation or bracket notation. Dot notation is the simplest way to access values, while bracket notation allows for more complex access patterns.
