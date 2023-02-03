---
title: Find the current year in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: The current year in JavaScript can be retrieved using the Date object`s getFullYear() method.
---

**Contents**

[TOC]

**Using the Date Object**

```javascript
let currentYear = new Date().getFullYear();
```

**Using Date.now()**

```javascript
let currentYear = new Date(Date.now()).getFullYear();
```

**Using getYear()**

```javascript
let currentYear = (new Date()).getYear() + 1900;
```

**Using toISOString()**

```javascript
let currentYear = new Date().toISOString().slice(0,4);
```
