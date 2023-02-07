---
title: Change spaces to hyphens and convert to lowercase
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Replace all spaces with dashes and convert all letters to lower-case by using the Javascript methods .replace() and .toLowerCase().
---

**Contents**

[TOC]

## Using `replace()`

The `replace()` method can be used to replace all occurrences of a substring with another substring.

```js
let str = 'Replace spaces with dashes';

str.replace(/ /g, '-').toLowerCase();
```

## Using `split()` and `join()`

The `split()` method can be used to split a string into an array of substrings, and the `join()` method can be used to join the elements of an array into a string.

```js
let str = 'Replace spaces with dashes';

str.split(' ').join('-').toLowerCase();
```

## Using `replace()` and `toLowerCase()`

The `replace()` method and the `toLowerCase()` method can be used together to replace all spaces with dashes and make all letters lower-case.

```js
let str = 'Replace spaces with dashes';

str.replace(/ /g, '-').toLowerCase();
```

## Using `map()`, `join()` and `toLowerCase()`

The `map()` method can be used to create a new array with the results of calling a provided function on every element in the array, the `join()` method can be used to join the elements of an array into a string, and the `toLowerCase()` method can be used to make all letters lower-case.

```js
let str = 'Replace spaces with dashes';

str.split(' ').map(x => x + '-').join('').toLowerCase();
```
