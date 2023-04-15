---
title: Iterate over an array in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: To loop through an array in JavaScript, use the for loop or forEach() method.
---

**Contents**

[TOC]

**For Loop**

```javascript
var array = ["a", "b", "c"];

for (var i = 0; i < array.length; i++) {
  console.log(array[i]);
}
```

**For...Of Loop**

```javascript
var array = ["a", "b", "c"];

for (var element of array) {
  console.log(element);
}
```

**ForEach Loop**

```javascript
var array = ["a", "b", "c"];

array.forEach(function(element) {
  console.log(element);
});
```

**For...In Loop**

```javascript
var array = ["a", "b", "c"];

for (var index in array) {
  console.log(array[index]);
}
```
