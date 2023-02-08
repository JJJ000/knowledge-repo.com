---
title: What is the procedure for replacing only captured groups?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: Use the String.prototype.replace() method with a regular expression that includes capture groups and a replacement string with backreferences.
---

**Contents**

[TOC]

1. Using String.prototype.replace()

The String.prototype.replace() method can be used to replace captured groups in a string. This method takes two arguments: a regular expression and a replacement string. The regular expression should include capture groups that will be replaced with the values in the replacement string.

2. Example

For example, given the following string:

```
var str = "John Doe is a software engineer";
```

We can use the following regular expression and replacement string to replace the captured groups with the values in the replacement string:

```
var regex = /(John) (Doe)/;
var replacement = "Jane Smith";
```

The resulting string will be:

```
var result = str.replace(regex, replacement);
// result is "Jane Smith is a software engineer"
```

3. Using String.prototype.replaceAll()

The String.prototype.replaceAll() method can also be used to replace captured groups in a string. This method takes two arguments: a regular expression and a replacement string. The regular expression should include capture groups that will be replaced with the values in the replacement string.

4. Example

For example, given the following string:

```
var str = "John Doe is a software engineer";
```

We can use the following regular expression and replacement string to replace the captured groups with the values in the replacement string:

```
var regex = /(John) (Doe)/;
var replacement = "Jane Smith";
```

The resulting string will be:

```
var result = str.replaceAll(regex, replacement);
// result is "Jane Smith is a software engineer"
```
