---
title: Jq does not allow accessing elements of an array using a string value
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: No, you cannot index an array with a string in JSON.
---

**Contents**

[TOC]

### Section 1: What is a Json Array?
A Json array is an ordered list of values. It is written in JavaScript Object Notation (JSON) and is used to store and transport data. It is composed of two square brackets that enclose a comma-separated list of values.

### Section 2: What is a String?
A string is a sequence of characters. It can contain any type of character, including numbers, symbols, and spaces. Strings are typically used to store and manipulate text.

### Section 3: Why Can't You Index an Array with a String?
Json arrays are indexed using numbers, not strings. This is because strings are not ordered in the same way as numbers. Therefore, attempting to index an array with a string will result in an error.

### Section 4: How Can You Work Around This?
If you need to index an array with a string, you can use a JavaScript object instead. A JavaScript object is a collection of key-value pairs, where the keys are strings and the values can be any type of data. This allows you to use strings as keys to access values in the object.
