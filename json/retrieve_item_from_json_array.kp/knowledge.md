---
title: Retrieve one element from a name-value JSON array
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-15 00:00:00
updated_at: 2023-02-15 00:00:00
tldr: To get one item from an array of name,value JSON, use the array index to access the desired item.
---

**Contents**

[TOC]

**Section 1: Accessing the Item**

To access an item from an array of name-value JSON, you can use the dot notation or bracket notation.

**Section 2: Dot Notation**

The dot notation is used to access the value of a property in an object. The syntax is: objectName.propertyName. For example, if you have an array of name-value JSON like this:

```
[
  {name: "John", age: 25},
  {name: "Jane", age: 30}
]
```

You can access the age of John using dot notation like this:

```
array[0].age
```

**Section 3: Bracket Notation**

The bracket notation is used to access the value of a property in an object using its name. The syntax is: objectName[propertyName]. For example, if you have an array of name-value JSON like this:

```
[
  {name: "John", age: 25},
  {name: "Jane", age: 30}
]
```

You can access the age of John using bracket notation like this:

```
array[0]["age"]
```

**Section 4: Conclusion**

In conclusion, you can access an item from an array of name-value JSON using either the dot notation or bracket notation.
