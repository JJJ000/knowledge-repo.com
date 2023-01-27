---
title: Forming strings spanning multiple lines in javascript
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Multiline strings in JavaScript can be created using template literals, denoted by backticks (`).
---

**Contents**

[TOC]

**Using the Backtick Character**

Multiline strings can be created in JavaScript by using the backtick character (`), also called the grave accent. The backtick character allows for strings to span multiple lines and preserves line breaks and other whitespace characters.

For example:

```
const multiLineString = `This is
a multiline
string.`
```

**Using the Plus (+) Operator**

Multiline strings can also be created using the plus (+) operator. This method involves concatenating multiple strings together using the plus operator.

For example:

```
const multiLineString = 'This is ' +
                        'a multiline ' +
                        'string.';
```

**Using Template Literals**

Multiline strings can also be created using Template Literals, which are denoted by the backtick character. Template Literals allow for the use of string interpolation, which can be useful for creating dynamic strings.

For example:

```
const name = 'John';
const multiLineString = `Hello,
my name is ${name}.`;
```

**Using the Join Method**

Multiline strings can also be created using the join() method. This method takes an array of strings as an argument and joins them together with a specified separator.

For example:

```
const lines = ['This is', 'a multiline', 'string.'];
const multiLineString = lines.join(' ');
```
