---
title: Convert a nil value to null using jsonencoder
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: JSONEncoder will encode nil values as null when encoding JSON.
---

**Contents**

[TOC]

**Section 1: What is JSONEncoder?**

JSONEncoder is a class in the Python Standard Library that is used to serialize a Python object into a JSON string. It provides an interface for converting an object to a JSON string representation.

**Section 2: How Does JSONEncoder Work?**

JSONEncoder works by taking an object and converting it into a JSON string representation. It does this by iterating over the object's attributes and encoding each attribute into a JSON string.

**Section 3: How Does JSONEncoder Handle Nil Values?**

JSONEncoder handles nil values by encoding them as null. This is done by setting the value of the attribute to null in the JSON string representation.

**Section 4: Examples of JSONEncoder Encoding Nil Values**

Examples of JSONEncoder encoding nil values include:

```
{
    "name": null
}
```

```
{
    "age": null
}
```
