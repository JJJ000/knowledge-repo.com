---
title: What is the syntax for using jq to filter an array of objects based on values in an inner array?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Use the `.[] | select(.inner\_array[].value == `desired\_value`)` filter to select objects from the array whose inner array contains a value equal to the desired value.
---

**Contents**

[TOC]

### Section 1: Overview 

jq is a command-line JSON processor that can be used to filter an array of objects based on values in an inner array. This can be done by combining the `map()` and `select()` functions. 

### Section 2: Syntax

The syntax for this operation is as follows:

```
jq '[<array of objects> | map(<inner array>) | select(<filter condition>)]'
```

### Section 3: Example

As an example, let's consider a JSON array of objects containing an inner array of numbers. We want to filter the objects based on the values in the inner array.

```json
[
  {
    "name": "John",
    "numbers": [1, 2, 3]
  },
  {
    "name": "Jane",
    "numbers": [4, 5, 6]
  },
  {
    "name": "Jack",
    "numbers": [7, 8, 9]
  }
]
```

The jq command to filter the objects based on the values in the inner array would be:

```
jq '[.[] | map(.numbers) | select(any(.; . > 5))]'
```

### Section 4: Output

The output of the above command would be:

```json
[
  {
    "name": "Jane",
    "numbers": [4, 5, 6]
  },
  {
    "name": "Jack",
    "numbers": [7, 8, 9]
  }
]
```
