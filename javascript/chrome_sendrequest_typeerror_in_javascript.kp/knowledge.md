---
title: There was an error when chrome attempted to send a request typeerror cannot convert a circular structure into json
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Circular structures cannot be serialized into JSON, so an error is thrown.
---

**Contents**

[TOC]

**Section 1: What is Circular Structure**
A circular structure is a data structure that contains a reference to itself, either directly or indirectly. This type of structure is often used in JavaScript to represent complex objects, such as linked lists or trees. It can also be used to represent a graph or network.

**Section 2: What is JSON**
JSON (JavaScript Object Notation) is a lightweight data-interchange format. It is a text-based, human-readable format for representing simple data structures and objects. It is often used to exchange data between a server and web application, as an alternative to XML.

**Section 3: What is the Error**
The TypeError occurs when a circular structure is encountered when trying to convert a JavaScript object into a JSON string. This is because the JSON format does not support circular references, so when an object contains a reference to itself, the conversion process fails.

**Section 4: How to Avoid the Error**
To avoid the TypeError, it is important to ensure that any data being converted to JSON does not contain any circular references. This can be done by using a library such as Lodash to clone the object before conversion, or by using the JSON.stringify() method and passing in a replacer function to replace any circular references with a placeholder.
