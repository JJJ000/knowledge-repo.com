---
title: Convert JavaScript seconds into a time string in hhmmss format
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can use the Date object to convert seconds to a time string with format hhmmss in JavaScript.
---

**Contents**

[TOC]

### Solution

#### Using Date Object

```javascript
function convertSecondsToTimeString(seconds) {
  const date = new Date(seconds * 1000);
  const hh = date.getUTCHours();
  const mm = date.getUTCMinutes();
  const ss = date.getSeconds();

  return `${hh}:${mm}:${ss}`;
}
```

#### Using Math

```javascript
function convertSecondsToTimeString(seconds) {
  const hh = Math.floor(seconds / 3600);
  const mm = Math.floor((seconds % 3600) / 60);
  const ss = Math.floor(seconds % 60);

  return `${hh}:${mm}:${ss}`;
}
```
