---
title: Iterate through an array in JavaScript using a for loop
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: To loop over an array in JavaScript, you can use the forEach() method.
---

**Contents**

[TOC]

**For Loop**

```
for (let i = 0; i < array.length; i++) {
  console.log(array[i]);
}
```

**For...of Loop**

```
for (const element of array) {
  console.log(element);
}
```

**For...in Loop**

```
for (const index in array) {
  console.log(array[index]);
}
```

**ForEach Loop**

```
array.forEach(element => {
  console.log(element);
});
```
