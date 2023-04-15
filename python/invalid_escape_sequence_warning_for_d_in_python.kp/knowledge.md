---
title: What is the alternative to \d as it triggers deprecationwarning due to an invalid escape sequence?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Use double backslashes to escape the backslash character, like `\\d`.
---

**Contents**

[TOC]

## Introduction
In Python, backslashes are used to escape characters in strings. The backslash itself must also be escaped with another backslash. `\d` is a regular expression pattern that matches any digit character. However, in some situations, using `\d` can raise a DeprecationWarning. This warning indicates that the pattern is using an invalid escape sequence. In this article, we will explore what causes this warning and suggest ways to fix it.

## Explanation
The DeprecationWarning regarding the invalid escape sequence can occur in Python because of a change in the way escape sequences are handled. Starting from Python 3.6, string literals that are preceded by the letter "f" are treated as f-strings. F-strings are a way of embedding expressions inside string literals, where the expressions are evaluated at runtime. 

For example, if we have the following code: 

```python
name = 'Alice'
print(f'Hello {name}!')
```

The output would be: 
```
Hello Alice!
```

In f-strings, backslashes followed by certain characters are treated as escape sequences, such as `\n` for a newline or `\t` for a tab. However, `\d` is not a valid escape sequence. Therefore, in f-strings, `\d` should be escaped explicitly using another backslash, like so: `\\d`.

## Example
Here is an example that causes the DeprecationWarning:
```python
import re

number = '123'
pattern = f'\d+'
match = re.match(pattern, number)
print(match.group())
```
The warning message produced by this code is:
```
DeprecationWarning: invalid escape sequence '\d'
```

To fix this warning, we can escape the `\d` by using double backslashes:
```python
import re

number = '123'
pattern = f'\\d+'
match = re.match(pattern, number)
print(match.group())
```

This will produce the expected output:
```
123
```

## Conclusion
In summary, if you encounter a DeprecationWarning regarding an invalid escape sequence with `\d`, it means that you are using it in an f-string without explicitly escaping it. To fix this warning, escape the `\d` by using two backslashes: `\\d`.
