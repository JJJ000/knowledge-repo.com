---
title: Reworded "substituting a number after the group identified by \number in python's re.sub."
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: It is used to refer to a previously matched group in the replacement string.
---

**Contents**

[TOC]

Introduction
---

The `re.sub()` function in Python is used to replace occurrences of a pattern in a string with a new string. It takes three arguments: the pattern to search for, the replacement string to replace the matches with, and the string to search through. The `re.sub()` function can use backreferences to refer to matched groups within the pattern. 

This article will explain how to use groups in the `re.sub()` function to reference a number after a matched group.

Using Groups in `re.sub()`
---

Groups in regular expressions are defined by enclosing a pattern in parentheses. The `re.sub()` function uses numbered backreferences to refer to matched groups in the pattern. For example, in the pattern `(a+)b\1`, the `+` modifier matches one or more occurrences of the letter `a`, and `\1` is a backreference to the first captured group.

If we want to reference a number after a matched group in `re.sub()`, we can use the syntax `\g<group_number>`, where `group_number` is the number of the capture group we want to reference. For example, if we have a pattern `"(\d+)-(\d+)"`, and we want to swap the order of the numbers using `re.sub()`, we can replace the pattern with `\g<2>-\g<1>`. This will match any string with two numbers separated by a hyphen, and replace it with the second number, followed by a hyphen, followed by the first number.

Example:
```python
import re

string = "42-99"
new_string = re.sub(r"(\d+)-(\d+)", r"\2-\1", string)

print(new_string) # "99-42"
```

Matching a Number After a Group in `re.sub()`
---

If we want to match a number that comes after a group using `re.sub()`, we first need to capture the group using parentheses. Then, we can add a pattern to match the number that comes after the group. We can use the `(?:)` syntax to make sure the pattern doesn't capture a new group.

Example:
```python
import re

string = "apple:3, orange:7, pear:5"
new_string = re.sub(r"(\w+):(\d+)(?:, (\w+):(\d+))?", r"\1:0.\2, \3:0.\4", string)

print(new_string) # "apple:0.3, orange:0.7, pear:0.5"
```

In this example, the pattern `"(\w+):(\d+)"` captures a word followed by a colon and a number. The optional pattern `(?:, (\w+):(\d+))?` matches a comma, followed by another word and number, but the entire pattern is optional. To reference the number after the first capture group, we use the syntax `\2`. To reference the second capture group, we use `\4`, and we use the `(?:)` syntax to make sure we don't capture a third group.

Conclusion
---

Groups in regular expressions are a powerful tool that can be used with the `re.sub()` function to perform complex pattern matching and string replacement. By using backreferences to captured groups, we can reference matches and submatches in our replacements. By using the `(?:)` syntax to avoid capturing unnecessary groups, we can make our patterns more efficient and easier to read.
