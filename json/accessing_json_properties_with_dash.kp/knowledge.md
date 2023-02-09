---
title: Unable to access JSON property containing a "-" dash
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-09 00:00:00
updated_at: 2023-02-09 00:00:00
tldr: JSON properties cannot contain a `-` dash, and must be accessed using bracket notation.
---

**Contents**

[TOC]

## Using Bracket Notation

Bracket notation is the most commonly used method for accessing JSON properties with dashes. It involves wrapping the property name in quotes and using square brackets to access the value associated with the property.

For example, if we had a JSON object with a property called `first-name`, we could access its value using the following notation:

```javascript
var jsonObj = {
  "first-name": "John"
};

var firstName = jsonObj["first-name"]; // John
```

## Using Dot Notation

Dot notation can also be used to access JSON properties with dashes. However, it is important to note that this method is not as widely supported as bracket notation, as some browsers may not recognize the property name if it contains a dash.

For example, if we had a JSON object with a property called `first-name`, we could access its value using the following notation:

```javascript
var jsonObj = {
  "first-name": "John"
};

var firstName = jsonObj.first-name; // John
```

## Pros and Cons

The primary advantage of using bracket notation to access JSON properties with dashes is that it is widely supported across all modern browsers. This makes it the preferred method for accessing such properties.

On the other hand, dot notation can be used to access JSON properties with dashes, but it is not as widely supported. Therefore, it is not recommended to use this method for accessing such properties.
