---
title: What is the origin of the names for javascript's "atob()" and "btoa()" functions?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: The names `atob()` and `btoa()` are derived from the terms `ASCII to binary` and `binary to ASCII`.
---

**Contents**

[TOC]

#### Meaning of "a" and "b"
The "a" and "b" in the `atob()` and `btoa()` functions stand for "ascii" and "binary". The `atob()` function converts a string of ascii characters to binary data, while the `btoa()` function converts binary data to a string of ascii characters.

#### Purpose of Functions
The purpose of the `atob()` and `btoa()` functions is to encode and decode data. The `atob()` function is used to decode data that has been encoded using the `btoa()` function. Conversely, the `btoa()` function is used to encode data that has been decoded using the `atob()` function.

#### Naming Convention
The naming convention for the `atob()` and `btoa()` functions follows the convention of other programming languages, such as C and Java. In these languages, the `atob()` and `btoa()` functions are usually named `atoi()` and `itoa()`, respectively. The "i" stands for "integer", which is the data type used for binary data.
