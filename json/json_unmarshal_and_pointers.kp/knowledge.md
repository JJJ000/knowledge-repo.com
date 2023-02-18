---
title: What is the difference between json.unmarshal working with references and not pointers?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: json.Unmarshal works with reference because it needs to modify the underlying value of the reference.
---

**Contents**

[TOC]

# Explanation

JSON is a data-interchange format that is used to represent data objects in a structured format. It is a text-based, human-readable format which can be easily parsed and converted into objects. Unmarshal is a function in the json package of the Go programming language which is used to parse a JSON-encoded data and store the result in a value or pointer.

# Reference vs Pointer

A reference is a type of data structure that stores the address of a variable, while a pointer is a type of data structure that stores the address of a memory location. A reference is used to refer to the same object, while a pointer is used to refer to an object at a different memory location.

# Why Unmarshal works with Reference

When json.Unmarshal is called, it takes in a reference to a data structure and uses this to parse the JSON-encoded data. Since the reference stores the address of the same object, the data can be easily parsed and stored in the same object.

# Why Unmarshal does not work with Pointer

When json.Unmarshal is called with a pointer, it takes in the address of a different memory location. Since the pointer stores the address of a different memory location, the data cannot be parsed and stored in the same object. Therefore, json.Unmarshal does not work with pointers.
