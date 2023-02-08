---
title: What is the process for looping through a JSON structure?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: You can iterate over a JSON structure by looping through the object`s keys or by using a library like jQuery or lodash.
---

**Contents**

[TOC]

1. Accessing Values

To iterate over a JSON structure, you can use the `for` loop to access each value in the structure. For example, if you have a JSON object like this:

```
{
  "name": "John",
  "age": 30,
  "hobbies": ["reading", "cooking", "hiking"]
}
```

You can use a `for` loop to access each value in the object:

```
for (let key in jsonObject) {
  let value = jsonObject[key];
  console.log(`${key}: ${value}`);
}
```

This will print out:

```
name: John
age: 30
hobbies: ["reading", "cooking", "hiking"]
```

2. Iterating Arrays

When iterating over an array of objects, you can use the `forEach` method to access each item in the array. For example, if you have an array of objects like this:

```
[
  {
    "name": "John",
    "age": 30
  },
  {
    "name": "Jane",
    "age": 25
  },
  {
    "name": "Bob",
    "age": 40
  }
]
```

You can use `forEach` to access each object in the array:

```
jsonArray.forEach((item) => {
  console.log(`Name: ${item.name}, Age: ${item.age}`);
});
```

This will print out:

```
Name: John, Age: 30
Name: Jane, Age: 25
Name: Bob, Age: 40
```

3. Nested Structures

For nested structures, you can use `for` loops to access each value in the structure. For example, if you have a JSON object like this:

```
{
  "name": "John",
  "age": 30,
  "hobbies": [
    {
      "name": "reading",
      "frequency": "daily"
    },
    {
      "name": "cooking",
      "frequency": "weekly"
    },
    {
      "name": "hiking",
      "frequency": "monthly"
    }
  ]
}
```

You can use a `for` loop to access each value in the object:

```
for (let key in jsonObject) {
  let value = jsonObject[key];
  if (Array.isArray(value)) {
    value.forEach((hobby) => {
      console.log(`Hobby: ${hobby.name}, Frequency: ${hobby.frequency}`);
    });
  } else {
    console.log(`${key}: ${value}`);
  }
}
```

This will print out:

```
name: John
age: 30
Hobby: reading, Frequency: daily
Hobby: cooking, Frequency: weekly
Hobby: hiking, Frequency: monthly
```

4. Parsing JSON

To parse a JSON string, you can use the `JSON.parse` method. For example, if you have a JSON string like this:

```
{
  "name": "John",
  "age": 30,
  "hobbies": ["reading", "cooking", "hiking"]
}
```

You can use `JSON.parse` to parse the string into an object:

```
let jsonObject = JSON.parse(jsonString);
```

This will create an object that you can then iterate over using the methods described above.
