---
title: What is the process for determining if a variable is defined in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can check if a variable is defined by using the `typeof` operator.
---

**Contents**

[TOC]

##### Using typeof Operator 
The typeof operator can be used to check if a variable is defined or not. The syntax is as follows:

```javascript
typeof variableName !== 'undefined'
```

If the variable is defined, the expression will return true, otherwise it will return false.

##### Using the in Operator 
The in operator can be used to check if a variable is defined or not. The syntax is as follows:

```javascript
variableName in window
```

If the variable is defined, the expression will return true, otherwise it will return false.

##### Using the hasOwnProperty() Method 
The hasOwnProperty() method can be used to check if a variable is defined or not. The syntax is as follows:

```javascript
window.hasOwnProperty('variableName')
```

If the variable is defined, the expression will return true, otherwise it will return false.
