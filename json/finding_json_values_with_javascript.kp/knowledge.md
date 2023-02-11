---
title: Find the value of a JSON object using javascript
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: The value of a JSON key can be accessed using dot notation or bracket notation.
---

**Contents**

[TOC]

### Using Dot Notation

We can use dot notation to access the value of a key in a JSON object. For example, if we have a JSON object like this:

```
{
  "name": "John Doe",
  "age": 20
}
```

We can access the value of the "name" key like this:

```
const name = jsonObject.name;
```

### Using Bracket Notation

We can also use bracket notation to access the value of a key in a JSON object. For example, if we have a JSON object like this:

```
{
  "name": "John Doe",
  "age": 20
}
```

We can access the value of the "name" key like this:

```
const name = jsonObject["name"];
```

### Using a Loop

We can also use a loop to iterate over the keys in a JSON object and access the values. For example, if we have a JSON object like this:

```
{
  "name": "John Doe",
  "age": 20
}
```

We can loop over the keys and access the values like this:

```
for (const key in jsonObject) {
  const value = jsonObject[key];
  console.log(value);
}
```

### Using a Library

Finally, we can also use a library like Lodash to access the values of a JSON object. For example, if we have a JSON object like this:

```
{
  "name": "John Doe",
  "age": 20
}
```

We can use Lodash to access the value of the "name" key like this:

```
const name = _.get(jsonObject, 'name');
```
