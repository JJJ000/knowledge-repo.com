---
title: Determine the final day of the month
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The last day of a month can be calculated by using the Date object`s getDate() and getMonth() methods to determine the last day of the current month.
---

**Contents**

[TOC]

# Solution 1

Using the Date object:

```javascript
const lastDayOfMonth = (year, month) => {
  const date = new Date(year, month + 1, 0);
  return date.getDate();
};
```

# Solution 2

Using the built-in getDay() method:

```javascript
const lastDayOfMonth = (year, month) => {
  const date = new Date(year, month, 0);
  return date.getDay();
};
```

# Solution 3

Using the built-in getMonth() method:

```javascript
const lastDayOfMonth = (year, month) => {
  const date = new Date(year, month + 1, 0);
  return date.getMonth();
};
```

# Solution 4

Using the built-in getFullYear() method:

```javascript
const lastDayOfMonth = (year, month) => {
  const date = new Date(year, month + 1, 0);
  return date.getFullYear();
};
```
