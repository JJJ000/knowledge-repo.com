---
title: How to correctly convert byte size to kilobytes, megabytes, and gigabytes using javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the built-in JavaScript functions toBytes(), toKB(), toMB(), and toGB() to convert size in bytes to KB, MB, and GB, respectively.
---

**Contents**

[TOC]

**Section 1: Defining the Size**

The size in bytes should first be defined in a variable. This can be done using either a number or a string.

**Section 2: Converting to KB**

To convert the size in bytes to kilobytes, the size should first be divided by 1024. This can be done using the following code:

```js
let kb = size / 1024;
```

**Section 3: Converting to MB**

To convert the size in bytes to megabytes, the size should first be divided by 1024 twice. This can be done using the following code:

```js
let mb = size / (1024 * 1024);
```

**Section 4: Converting to GB**

To convert the size in bytes to gigabytes, the size should first be divided by 1024 three times. This can be done using the following code:

```js
let gb = size / (1024 * 1024 * 1024);
```
