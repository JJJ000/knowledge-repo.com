---
title: Retrieving the present date and time in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The current date and time can be retrieved using the Date object in JavaScript.
---

**Contents**

[TOC]

# Date

To get the current date in JavaScript, use the `Date()` method. This will return the current date in the format `YYYY-MM-DD`.

```javascript
let currentDate = new Date();
console.log(currentDate); // Outputs: 2020-03-02
```

# Time

To get the current time in JavaScript, use the `Date()` method. This will return the current time in the format `HH:MM:SS`.

```javascript
let currentTime = new Date();
console.log(currentTime); // Outputs: 11:35:26
```

# Date and Time

To get the current date and time in JavaScript, use the `Date()` method. This will return the current date and time in the format `YYYY-MM-DD HH:MM:SS`.

```javascript
let currentDateTime = new Date();
console.log(currentDateTime); // Outputs: 2020-03-02 11:35:26
```
