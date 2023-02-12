---
title: What is the process for retrieving the name and value of a JSON object?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: Use the dot notation (objectName.propertyName) or bracket notation (objectName[`propertyName`]) to access JSON object name/value.
---

**Contents**

[TOC]

### Accessing JSON Objects

1. Using dot notation: Dot notation is the most common way to access JSON objects. This involves specifying the name of the object followed by a period and the name of the property you want to access. For example, if we wanted to access the value of the "name" property of the following JSON object: 

```
{
    "name": "John Doe",
    "age": 25
}
```

We would use the following syntax:

```
objectName.name
```

2. Using bracket notation: Bracket notation is an alternative way to access JSON objects. This involves specifying the name of the object followed by brackets containing the name of the property you want to access. For example, if we wanted to access the value of the "name" property of the above JSON object, we would use the following syntax:

```
objectName["name"]
```

3. Using the get() method: The get() method is another way to access JSON objects. This involves calling the get() method on the object and passing in the name of the property you want to access. For example, if we wanted to access the value of the "name" property of the above JSON object, we would use the following syntax:

```
objectName.get("name")
```

4. Using the for...in loop: The for...in loop is a way to iterate through JSON objects. This involves looping through the object and accessing the properties using dot notation or bracket notation. For example, if we wanted to access the value of the "name" property of the above JSON object, we would use the following syntax:

```
for (let prop in objectName) {
    console.log(objectName[prop]);
}
```
