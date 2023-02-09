---
title: What is the syntax for a JSON array of strings?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: A JSON array of strings is represented as an array of string values enclosed in square brackets.
---

**Contents**

[TOC]

## Section 1: Syntax
A JSON array of strings is represented as a list of strings within a set of square brackets `[]`.

## Section 2: Example
For example, the following is a valid JSON array of strings:
```json
["string1", "string2", "string3"]
```

## Section 3: Nested Arrays
It is also possible to create nested arrays of strings, like so:
```json
[["string1", "string2"], ["string3", "string4"]]
```

## Section 4: Data Types
Note that when representing strings in JSON, the data type must be specified as a string. For example, the following is not valid JSON:
```json
[1, 2, 3]
```
This should instead be written as:
```json
["1", "2", "3"]
```
