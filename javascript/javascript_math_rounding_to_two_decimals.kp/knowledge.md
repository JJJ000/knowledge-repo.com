---
title: Round JavaScript numbers to two decimal places
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To round a number to two decimal places in JavaScript, use the toFixed() method.
---

**Contents**

[TOC]

### Method 1:

```javascript
Math.round(num * 100) / 100
```

### Method 2:

```javascript
(Math.round(num * 100) / 100).toFixed(2)
```

### Method 3:

```javascript
Number(num.toFixed(2))
```

### Method 4:

```javascript
parseFloat(num.toFixed(2))
```
