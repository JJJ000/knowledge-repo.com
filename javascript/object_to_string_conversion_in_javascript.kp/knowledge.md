---
title: Transforming an object into a string
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: An object can be converted to a string in Javascript by using the JSON.stringify() method.
---

**Contents**

[TOC]

# Stringify

The most common way to convert an object to a string in JavaScript is to use the built-in `JSON.stringify()` method. This method takes a JavaScript object and returns a JSON string representation of it.

# Syntax

The syntax for the `JSON.stringify()` method is as follows:

```javascript
JSON.stringify(value[, replacer[, space]])
```

Where `value` is the object to be converted to a string, `replacer` is an optional parameter used to transform values before they are stringified, and `space` is an optional parameter used to add white space to the stringified result.

# Example

For example, consider the following JavaScript object:

```javascript
let person = {
  name: 'John Doe',
  age: 30
};
```

We can convert this object to a string using the `JSON.stringify()` method:

```javascript
let personString = JSON.stringify(person);

console.log(personString); // '{"name":"John Doe","age":30}'
```

# Output

The output of the `JSON.stringify()` method is a JSON string representation of the object.
