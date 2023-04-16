---
title: What is the difference between using dot notation and brackets to access properties in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Dot notation is used to access properties of an object, while brackets are used to access properties of an object using a string or a variable.
---

**Contents**

[TOC]

#### Dot Notation
Dot notation is the most common way of accessing properties in JavaScript. It involves using a dot (.) followed by the name of the property. For example, if you have an object called "person" and you want to access the name property, you would use the following code:

person.name

This will return the value associated with the name property of the person object.

#### Brackets Notation
Brackets notation is an alternate way of accessing properties in JavaScript. It involves using brackets ([]) followed by the name or index of the property. For example, if you have an array called "numbers" and you want to access the second element, you would use the following code:

numbers[1]

This will return the value associated with the second element of the numbers array.

#### Advantages of Dot Notation
Dot notation is generally easier to read and understand than brackets notation. It is also more concise, making it easier to write code quickly.

#### Advantages of Brackets Notation
Brackets notation can be used to access properties that have names that are not valid identifiers. This can be useful when working with certain data structures, such as JSON objects. It can also be used to access properties that are stored as strings, which is not possible with dot notation.
