---
title: An ecmascript 6 arrow function that produces an object as its output
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: A arrow function can return an object by enclosing the object in parentheses, e.g. const myObject = () => ({key value});
---

**Contents**

[TOC]

#### Syntax

`const myObject = () => ({key: value});`

#### Example

`const myObject = () => ({name: "John", age: 28});`

#### Explanation

This syntax uses an arrow function to return an object. The object is wrapped in parentheses and contains key-value pairs separated by a comma. 

#### Usage

This syntax can be used to quickly create and return an object. It is especially useful when the object is a simple one with only a few key-value pairs.
