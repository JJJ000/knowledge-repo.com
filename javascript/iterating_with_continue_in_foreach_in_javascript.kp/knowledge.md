---
title: 'proceed' in cursor.foreach()
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: No, `continue` is not used in cursor.forEach() in Javascript.
---

**Contents**

[TOC]

**Section 1: What is Cursor.forEach()?**
Cursor.forEach() is a method in the MongoDB Node.js driver that allows for the iteration of documents in a MongoDB collection. It is used to loop through the documents in a collection and perform an operation on each document.

**Section 2: What Does "Continue" Do?**
The "continue" keyword is used in the cursor.forEach() method to skip the remainder of the current iteration of the loop and move on to the next iteration. This allows the loop to skip documents that do not meet certain criteria.

**Section 3: How Does "Continue" Work?**
When the "continue" keyword is used in the cursor.forEach() loop, the loop will skip the remainder of the code in the loop and move on to the next iteration. This allows the loop to skip any documents that do not meet the criteria specified in the loop.

**Section 4: Examples of Using "Continue" in Cursor.forEach()**
Here is an example of using the "continue" keyword in the cursor.forEach() loop:

```
cursor.forEach(function(doc) {
  if (doc.age < 18) {
    continue;
  }
  // Do something with the document
});
```

In this example, the loop will skip any documents that have an age less than 18.
