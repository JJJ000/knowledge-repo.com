---
title: Add a prefix of zeroes to a date using javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: You can use the JavaScript toLocaleString() method to add leading zeroes to a date.
---

**Contents**

[TOC]

# Section 1: Using the Date.prototype.padStart() Method

The Date.prototype.padStart() method is a way to add leading zeroes to a date. This method takes two arguments, the first being the minimum length of the string, and the second being the character to use for padding. The following example illustrates how to use this method to add leading zeroes to a date:

```javascript
let date = new Date();
let day = date.getDate().toString().padStart(2, '0');
let month = (date.getMonth() + 1).toString().padStart(2, '0');
let year = date.getFullYear().toString().padStart(4, '0');

let formattedDate = `${day}/${month}/${year}`;
console.log(formattedDate); // Outputs "DD/MM/YYYY"
```

# Section 2: Using the String.prototype.padStart() Method

The String.prototype.padStart() method is another way to add leading zeroes to a date. This method also takes two arguments, the first being the minimum length of the string, and the second being the character to use for padding. The following example illustrates how to use this method to add leading zeroes to a date:

```javascript
let date = new Date();
let day = date.getDate().toString();
let month = (date.getMonth() + 1).toString();
let year = date.getFullYear().toString();

let formattedDate = `${day.padStart(2, '0')}/${month.padStart(2, '0')}/${year.padStart(4, '0')}`;
console.log(formattedDate); // Outputs "DD/MM/YYYY"
```

# Section 3: Using the toLocaleDateString() Method

The toLocaleDateString() method is a way to format a date in a specific locale. This method takes two arguments, the first being the locale to use for formatting, and the second being an object containing options for formatting. The following example illustrates how to use this method to add leading zeroes to a date in the en-US locale:

```javascript
let date = new Date();
let formattedDate = date.toLocaleDateString('en-US', {
  day: '2-digit',
  month: '2-digit',
  year: 'numeric'
});

console.log(formattedDate); // Outputs "MM/DD/YYYY"
```

# Section 4: Using the toISOString() Method

The toISOString() method is a way to format a date in the ISO 8601 format. This method does not take any arguments and will always return a date in the ISO format. The following example illustrates how to use this method to add leading zeroes to a date:

```javascript
let date = new Date();
let formattedDate = date.toISOString().replace(/T.*/, '');

console.log(formattedDate); // Outputs "YYYY-MM-DD"
```
