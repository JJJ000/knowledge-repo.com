---
title: Error when trying to convert an object with circular references into JSON in node.js
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: Circular structures cannot be stringified into JSON, so they must be handled before attempting to stringify.
---

**Contents**

[TOC]

### What is a Circular Structure?
A circular structure is a data structure in which a set of nodes are connected in a circular fashion. This means that each node is connected to the next node in the list, and the last node is connected to the first node.

### What is JSON?
JSON (JavaScript Object Notation) is a lightweight data-interchange format. It is a text-based, human-readable format for representing simple data structures and objects. JSON is often used for data exchange between a server and a web application.

### What is a TypeError?
A TypeError is an error that occurs when a value is not of the expected type. For example, if a function expects a number as an argument, but a string is passed in, a TypeError will be thrown.

### How to Solve the Problem?
The best way to solve the problem of converting a circular structure to JSON in Node.js is to use a library like json-stringify-safe. This library will detect circular structures in the data and convert them to a string representation instead of throwing a TypeError. Additionally, you can use a library like json-cycle to detect and break circular references in the data.
