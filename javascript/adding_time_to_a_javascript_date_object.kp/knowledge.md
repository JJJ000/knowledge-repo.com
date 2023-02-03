---
title: What is the syntax for increasing a JavaScript date object by 30 minutes?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the Date.setMinutes() method to add 30 minutes to a Date object.
---

**Contents**

[TOC]

1. Create Date Object 
```javascript
let date = new Date();
```

2. Add Minutes 
```javascript
date.setMinutes(date.getMinutes() + 30);
```

3. Output Date 
```javascript
console.log(date);
```

4. Format Date 
```javascript
let formattedDate = date.toLocaleString();
```
