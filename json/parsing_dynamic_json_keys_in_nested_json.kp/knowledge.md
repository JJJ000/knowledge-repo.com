---
title: What is the best way to extract data from a nested JSON response that contains a dynamic key?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: You can parse a dynamic JSON key in a nested JSON result by using a combination of the JSON object`s keys and a loop to iterate through the nested structure.
---

**Contents**

[TOC]

# Section 1: Accessing Nested JSON

When accessing nested JSON, you need to use a combination of the dot notation and bracket notation. The dot notation is used to access the values of keys in the top level of the JSON object, while the bracket notation is used to access the values of keys in the nested levels of the JSON object.

# Section 2: Parsing a Dynamic JSON Key

When parsing a dynamic JSON key, you need to use the bracket notation to access the value of the key. This is because the key is not known until runtime, so it cannot be accessed using the dot notation.

# Section 3: Example

For example, let's say we have the following JSON object:

```json
{
  "data": {
    "user1": {
      "name": "John Doe"
    },
    "user2": {
      "name": "Jane Doe"
    }
  }
}
```

To access the name of user1, we can use the following code:

```js
const user1Name = jsonObject.data["user1"].name;
```

# Section 4: Conclusion

In conclusion, when accessing nested JSON, you need to use a combination of the dot notation and bracket notation. When parsing a dynamic JSON key, you need to use the bracket notation to access the value of the key.
