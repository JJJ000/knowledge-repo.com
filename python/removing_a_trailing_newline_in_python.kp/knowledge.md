---
title: What is the best way to get rid of a trailing newline?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the `rstrip()` method to remove any trailing newline characters from a string.
---

**Contents**

[TOC]

#1 Using `rstrip()`
The `rstrip()` method can be used to remove any trailing whitespace characters (including newlines) from the end of a string.

#2 Example
The following example shows how to use `rstrip()` to remove a trailing newline from a string:

```
s = 'Hello World!\n'
s = s.rstrip('\n')
print(s)
```

#3 Output
The output of the above code will be:

```
Hello World!
```

#4 Notes
It is important to note that `rstrip()` does not modify the original string, it only returns a new string with the whitespace removed.
