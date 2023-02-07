---
title: Assign a new property to a JavaScript object using a variable as the key
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can add a property to a JavaScript object using a variable as the name by using bracket notation, e.g. object[variableName] = value;
---

**Contents**

[TOC]

**Section 1: Declare the Object**

```javascript
let myObject = {};
```

**Section 2: Declare the Property Name Variable**

```javascript
let propertyName = 'name';
```

**Section 3: Add the Property to the Object**

```javascript
myObject[propertyName] = 'John Doe';
```

**Section 4: Log the Object**

```javascript
console.log(myObject);
```

The console will log `{name: "John Doe"}`.
