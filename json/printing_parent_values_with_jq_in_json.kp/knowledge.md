---
title: How can I output the parent value of an object when I am already within the object's nested elements using jq?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: You can use the `..` operator to access the parent value of an object.
---

**Contents**

[TOC]

**Section 1 - Accessing the Parent Object**

One way to access the parent object from a nested child object is to use the `parent()` method. This method will traverse up the parent chain and return the parent object.

**Section 2 - Using the Parent Object**

Once the parent object is accessed, it can be used in various ways. For example, the `each()` function can be used to iterate through each property of the parent object and print out its value.

**Section 3 - Using the Parent Object in a Loop**

Another way to use the parent object is to use it in a loop. The loop can be used to iterate through each property of the parent object and print out its value.

**Section 4 - Printing the Parent Object**

Once the parent object is accessed, it can be printed out using the `console.log()` function. This can be used to print out the entire parent object or just specific properties of the parent object.
