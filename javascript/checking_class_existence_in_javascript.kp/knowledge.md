---
title: How to determine if an element has a specific class in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: You can check if an element contains a class in JavaScript by using the element`s classList property and the includes() method.
---

**Contents**

[TOC]

**Using the .classList Property:**

1. Retrieve the element's classList property.

```javascript
let elementClasses = element.classList;
```

2. Use the includes() method to check if the class is present in the classList.

```javascript
elementClasses.includes('className');
```

**Using the .className Property:**

1. Retrieve the element's className property.

```javascript
let elementClassName = element.className;
```

2. Use the search() method to check if the class is present in the className.

```javascript
elementClassName.search('className') !== -1;
```
