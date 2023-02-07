---
title: What is the syntax for getting the current date in the format dd/mm/yyyy in JavaScript and adding it to an input field?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the Date() object`s .toLocaleDateString() method to get the current date in the desired format and then use the .value property of the input element to set the value of the input.
---

**Contents**

[TOC]

### 1. Create a Date Object

Creating a Date object is the first step in getting the current date. The Date object is used to work with dates and times. 

```javascript
let currentDate = new Date();
```

### 2. Format the Date

The Date object can be formatted to display the current date in dd/mm/yyyy format. This can be done using the `toLocaleDateString()` function.

```javascript
let date = currentDate.toLocaleDateString();
```

### 3. Append Date to Input

Once the date has been formatted, it can be appended to the input field. This can be done using the `value` property of the input element.

```javascript
let input = document.getElementById("date");
input.value = date;
```

### 4. Output

The output should be the current date in the dd/mm/yyyy format appended to the input element.

```
<input type="text" id="date" value="01/01/2020">
```
