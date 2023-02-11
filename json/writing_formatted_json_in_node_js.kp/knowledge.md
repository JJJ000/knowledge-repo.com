---
title: Create a JSON object in Node.js with formatting
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: Node.js has a built-in JSON.stringify() function that can be used to format JSON.
---

**Contents**

[TOC]

**Section 1: Formatting JSON**

In Node.js, JSON can be formatted using the `JSON.stringify()` method. This method takes a JavaScript object as an argument and returns a string representation of the JSON data.

**Section 2: Example Usage**

For example, to format the following JSON object:

```
{
  "name": "John Doe",
  "age": 30
}
```

The code would look like this:

```
const jsonData = {
  "name": "John Doe",
  "age": 30
};

const jsonString = JSON.stringify(jsonData);

console.log(jsonString);
```

**Section 3: Output**

The output of the above code would be:

`{"name":"John Doe","age":30}`

**Section 4: Pretty Printing**

The `JSON.stringify()` method also supports a second argument, which is an optional replacer function that can be used to format the output as a "pretty-printed" JSON string.

For example, the following code would output the same JSON object as above, but with the data indented for readability:

```
const jsonData = {
  "name": "John Doe",
  "age": 30
};

const jsonString = JSON.stringify(jsonData, null, 2);

console.log(jsonString);
```

**Section 5: Output**

The output of the above code would be:

```
{
  "name": "John Doe",
  "age": 30
}
```
