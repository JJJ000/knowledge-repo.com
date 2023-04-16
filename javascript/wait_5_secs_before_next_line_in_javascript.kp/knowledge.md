---
title: Pause for 5 seconds before proceeding to the next line
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: setTimeout(function(){}, 5000);
---

**Contents**

[TOC]

## setTimeout

```javascript
setTimeout(function(){
  // code here
}, 5000);
```

## setInterval

```javascript
let count = 0;
const intervalId = setInterval(function(){
  count++;
  if (count === 5) {
    // code here
    clearInterval(intervalId);
  }
}, 1000);
```
