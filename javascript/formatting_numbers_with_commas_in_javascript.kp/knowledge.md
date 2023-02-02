---
title: What is the proper way to add commas to a number to indicate thousands?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Use the toLocaleString() method to format a number with commas as thousands separators in Javascript.
---

**Contents**

[TOC]

## Using toLocaleString()

The toLocaleString() method can be used to format a number with commas as thousands separators in Javascript. The toLocaleString() method converts a number into a string, representing the number in a given locale.

Syntax:

```
number.toLocaleString(locale, options);
```

Example:

```
var num = 1234567.89;

// US locale
num.toLocaleString('en-US'); // "1,234,567.89"

// German locale
num.toLocaleString('de-DE'); // "1.234.567,89"
```

## Using Regular Expressions

Regular expressions can also be used to format a number with commas as thousands separators in Javascript.

Syntax:

```
num.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",");
```

Example:

```
var num = 1234567.89;

num.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ","); // "1,234,567.89"
```

## Using Intl.NumberFormat

The Intl.NumberFormat() method can also be used to format a number with commas as thousands separators in Javascript. The Intl.NumberFormat() method formats a number according to the locale and formatting options of the specified locale.

Syntax:

```
new Intl.NumberFormat(locale, options).format(number);
```

Example:

```
var num = 1234567.89;

// US locale
new Intl.NumberFormat('en-US').format(num); // "1,234,567.89"

// German locale
new Intl.NumberFormat('de-DE').format(num); // "1.234.567,89"
```
