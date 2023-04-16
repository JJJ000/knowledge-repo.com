---
title: Delete empty properties from an object in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the delete operator to remove blank attributes from an object in Javascript.
---

**Contents**

[TOC]

### Using for Loop

```javascript
const removeBlankAttributes = obj => {
  for (let key in obj) {
    if (obj[key] === '') {
      delete obj[key];
    }
  }
  return obj;
};
```

### Using Object.keys()

```javascript
const removeBlankAttributes = obj => {
  Object.keys(obj).forEach(key => {
    if (obj[key] === '') {
      delete obj[key];
    }
  });
  return obj;
};
```

### Using Object.entries()

```javascript
const removeBlankAttributes = obj => {
  Object.entries(obj).forEach(([key, value]) => {
    if (value === '') {
      delete obj[key];
    }
  });
  return obj;
};
```

### Using Object.values()

```javascript
const removeBlankAttributes = obj => {
  Object.values(obj).forEach(value => {
    if (value === '') {
      delete obj[key];
    }
  });
  return obj;
};
```
