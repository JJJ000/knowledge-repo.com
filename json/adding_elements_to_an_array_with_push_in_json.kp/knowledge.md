---
title: Does array.push() exist?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: You cannot directly push to a JSON object; you would need to convert it to an array first.
---

**Contents**

[TOC]

**Section 1: Overview**

Adding elements to a JSON array is a fairly straightforward process. It involves using the Array.push() method, which adds an element to the end of an array. This method is useful when you want to add a new element to an existing JSON array without having to rewrite the entire array.

**Section 2: Syntax**

The syntax for using the Array.push() method is as follows:

```
myArray.push(element);
```

Where "myArray" is the name of the array, and "element" is the element you want to add.

**Section 3: Example**

For example, if you have a JSON array like this:

```
var myArray = [1, 2, 3];
```

You can add a new element, 4, to the end of the array like this:

```
myArray.push(4);
```

The resulting array would look like this:

```
[1, 2, 3, 4]
```

**Section 4: Conclusion**

In conclusion, the Array.push() method is a simple and effective way to add elements to a JSON array. It is important to remember that the element will be added to the end of the array, so if you want to add it at a specific index, you will need to use a different method.
