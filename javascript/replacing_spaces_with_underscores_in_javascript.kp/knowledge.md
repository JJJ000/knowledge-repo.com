---
title: Changing spaces to underscores in javascript?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: Use the String.replace() method to replace spaces with underscores.
---

**Contents**

[TOC]

##### Using the Replace Method

The `replace()` method can be used to replace spaces with underscores. This method takes two parameters: the substring to be replaced and the substring to replace it with. The following code snippet shows how this can be done:

```javascript
let myString = 'Hello World';
let newString = myString.replace(' ', '_');
console.log(newString); // Outputs 'Hello_World'
```

##### Using a Regular Expression

The `replace()` method can also be used with regular expressions to replace multiple spaces with underscores. The following code snippet shows how this can be done:

```javascript
let myString = 'Hello  World';
let newString = myString.replace(/\s+/g, '_');
console.log(newString); // Outputs 'Hello_World'
```

##### Using a For Loop

A `for` loop can also be used to replace spaces with underscores. The following code snippet shows how this can be done:

```javascript
let myString = 'Hello World';
let newString = '';

for (let i = 0; i < myString.length; i++) {
    if (myString[i] === ' ') {
        newString += '_';
    } else {
        newString += myString[i];
    }
}

console.log(newString); // Outputs 'Hello_World'
```
