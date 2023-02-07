---
title: Replace all instances of commas in a string using javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the String.prototype.replace() method to replace all commas in a string with a desired character or string.
---

**Contents**

[TOC]

**Solution 1: Using the Replace Method**

```javascript
var str = "Hello, World!";
var replaced = str.replace(/,/g, "");
console.log(replaced); // Outputs "Hello World!"
```

**Solution 2: Using Regular Expressions**

```javascript
var str = "Hello, World!";
var replaced = str.replace(/\,/g, "");
console.log(replaced); // Outputs "Hello World!"
```

**Solution 3: Using a For Loop**

```javascript
var str = "Hello, World!";
var replaced = "";
for (var i = 0; i < str.length; i++) {
  if (str[i] !== ",") {
    replaced += str[i];
  }
}
console.log(replaced); // Outputs "Hello World!"
```

**Solution 4: Using the Split and Join Methods**

```javascript
var str = "Hello, World!";
var replaced = str.split(",").join("");
console.log(replaced); // Outputs "Hello World!"
```
