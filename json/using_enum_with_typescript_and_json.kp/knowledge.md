---
title: Convert a JSON string into a typescript enumeration
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-12 00:00:00
updated_at: 2023-02-12 00:00:00
tldr: No, it is not possible to create a TypeScript enum from a JSON string.
---

**Contents**

[TOC]

**Section 1: Introduction**

Enums are a data type used to define a set of related constants. They are commonly used in programming languages to represent a set of related values, such as the days of the week, or the states of a process. In TypeScript, enums can be created from a JSON string using the `enum` keyword. This article will explain how to create an enum from a JSON string in TypeScript.

**Section 2: Creating an enum from a JSON string**

Creating an enum from a JSON string in TypeScript is relatively straightforward. First, the JSON string must be parsed into a JavaScript object. This can be done using the `JSON.parse()` method. Once the JSON string has been parsed into an object, the `enum` keyword can be used to create an enum from the object. The following example demonstrates this process:

```
let jsonString = '{ "Monday": 1, "Tuesday": 2, "Wednesday": 3 }';
let parsedObject = JSON.parse(jsonString);
enum DaysOfWeek = parsedObject;
```

**Section 3: Using the enum**

Once the enum has been created, it can be used in TypeScript code to access the values of the enum. The following example demonstrates how to use the `DaysOfWeek` enum created in the previous example:

```
let day = DaysOfWeek.Monday;
console.log(day); // 1
```

**Section 4: Conclusion**

In conclusion, enums can be created from a JSON string in TypeScript using the `enum` keyword. Once the enum has been created, it can be used in TypeScript code to access the values of the enum.
