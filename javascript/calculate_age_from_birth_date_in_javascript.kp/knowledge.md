---
title: Find the age given the birth date in the yyyymmdd format
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: You can calculate age by subtracting the birth date from the current date and dividing the result by 365.25.
---

**Contents**

[TOC]

# Solution

## 1. Calculate Age

We can use the following code to calculate the age given the birth date in the format YYYYMMDD:

```javascript
function calculateAge(birthDate) {
  const today = new Date();
  const birthYear = parseInt(birthDate.substring(0, 4));
  const birthMonth = parseInt(birthDate.substring(4, 6));
  const birthDay = parseInt(birthDate.substring(6, 8));

  let age = today.getFullYear() - birthYear;
  const monthDifference = today.getMonth() - birthMonth;

  if (monthDifference < 0 || (monthDifference === 0 && today.getDate() < birthDay)) {
    age--;
  }

  return age;
}
```

## 2. Usage

To use the above code, we can call the `calculateAge` function with a string argument in the format YYYYMMDD:

```javascript
const birthDate = '19870203';
const age = calculateAge(birthDate);
console.log(age); // 33
```

## 3. Edge Cases

The above code assumes that the birth date is in the valid format YYYYMMDD. If the argument is not a string or is not in the correct format, the code will throw an error.

## 4. Further Improvements

We can further improve the code by adding additional checks to make sure that the argument is in the correct format and handle edge cases such as leap years.
