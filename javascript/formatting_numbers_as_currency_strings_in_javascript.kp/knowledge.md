---
title: What is the best way to display numbers as currency strings?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the Intl.NumberFormat() method with the style set to `currency` to format numbers as currency strings in Javascript.
---

**Contents**

[TOC]

### Using toLocaleString()

The `toLocaleString()` method can be used to format numbers as currency strings. It takes an object as an argument, which can be used to specify the currency and other locale-specific formatting options.

For example, the following code formats a number as a US dollar string:

```js
const usd = 12345.67;
const usdString = usd.toLocaleString('en-US', { style: 'currency', currency: 'USD' });
console.log(usdString); // "$12,345.67"
```

### Using Intl.NumberFormat

The `Intl.NumberFormat` constructor can also be used to format numbers as currency strings. It takes an object as an argument, which can be used to specify the currency and other locale-specific formatting options.

For example, the following code formats a number as a US dollar string:

```js
const usd = 12345.67;
const usdString = new Intl.NumberFormat('en-US', { style: 'currency', currency: 'USD' }).format(usd);
console.log(usdString); // "$12,345.67"
```

### Using a Library

Another option is to use a library such as [accounting.js](http://openexchangerates.github.io/accounting.js/). This library provides a `formatMoney()` method which can be used to format numbers as currency strings.

For example, the following code formats a number as a US dollar string:

```js
const usd = 12345.67;
const usdString = accounting.formatMoney(usd, { symbol: '$',  format: '%s %v' });
console.log(usdString); // "$12,345.67"
```
