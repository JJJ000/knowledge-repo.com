---
title: Expressing logic as data in JSON format
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-11 00:00:00
updated_at: 2023-02-11 00:00:00
tldr: JSON can represent logic as data by using objects and arrays to store values and conditions.
---

**Contents**

[TOC]

**Section 1: Boolean Values**

JSON supports boolean values, which are either true or false. These can be represented as follows:

```json
{
  "isTrue": true,
  "isFalse": false
}
```

**Section 2: Logical Operators**

JSON also supports logical operators, such as AND, OR, and NOT. These can be represented as follows:

```json
{
  "operator": "AND",
  "operands": [
    {
      "isTrue": true
    },
    {
      "isFalse": false
    }
  ]
}
```

**Section 3: Conditionals**

JSON also supports conditionals, which are used to evaluate a statement based on a given condition. These can be represented as follows:

```json
{
  "condition": {
    "isTrue": true
  },
  "then": {
    "action": "doSomething"
  },
  "else": {
    "action": "doSomethingElse"
  }
}
```

**Section 4: Complex Logic**

Finally, JSON also supports complex logic, which can be represented as a series of conditionals and logical operators. For example:

```json
{
  "operator": "AND",
  "operands": [
    {
      "condition": {
        "isTrue": true
      },
      "then": {
        "action": "doSomething"
      },
      "else": {
        "action": "doSomethingElse"
      }
    },
    {
      "condition": {
        "isFalse": false
      },
      "then": {
        "action": "doSomethingElse"
      },
      "else": {
        "action": "doSomethingDifferent"
      }
    }
  ]
}
```
