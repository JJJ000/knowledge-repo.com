---
title: How can I use ng-repeat to iterate a specific number of times instead of looping through an array?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use a for loop to iterate over a range of numbers and perform the desired operation each time.
---

**Contents**

[TOC]

## For Loop
The most straightforward way to ng-repeat a defined number of times is to use a for loop. The code below will ng-repeat the number of times specified in the `num` variable.

```javascript
for (var i = 0; i < num; i++) {
    // ng-repeat code here
}
```

## While Loop
Another way to ng-repeat a defined number of times is to use a while loop. The code below will ng-repeat the number of times specified in the `num` variable.

```javascript
var i = 0;
while (i < num) {
    // ng-repeat code here
    i++;
}
```

## Array.forEach()
Another way to ng-repeat a defined number of times is to use the `Array.forEach()` method. The code below will ng-repeat the number of times specified in the `num` variable.

```javascript
Array(num).fill().forEach(function() {
    // ng-repeat code here
});
```

## Array.map()
The final way to ng-repeat a defined number of times is to use the `Array.map()` method. The code below will ng-repeat the number of times specified in the `num` variable.

```javascript
Array(num).fill().map(function() {
    // ng-repeat code here
});
```
