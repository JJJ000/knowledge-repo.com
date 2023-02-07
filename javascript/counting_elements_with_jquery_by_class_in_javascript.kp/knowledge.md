---
title: What is the most efficient way to count elements by class using jquery?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The best way to count elements by class in Javascript is to use the document.getElementsByClassName() method.
---

**Contents**

[TOC]

**Using for Loop**

1. Get the elements by class name:

```javascript
const elements = document.getElementsByClassName('className');
```

2. Create a counter variable and initialize it to 0:

```javascript
let count = 0;
```

3. Iterate over the elements array and increment the counter for each element:

```javascript
for (let i = 0; i < elements.length; i++) {
    count++;
}
```

4. Output the count:

```javascript
console.log(count);
```

**Using Array.prototype.filter()**

1. Get the elements by class name:

```javascript
const elements = document.getElementsByClassName('className');
```

2. Create an array from the elements array:

```javascript
const elementsArray = Array.from(elements);
```

3. Filter the array for elements that match the class name:

```javascript
const filteredArray = elementsArray.filter(element => element.className === 'className');
```

4. Output the length of the filtered array:

```javascript
console.log(filteredArray.length);
```
