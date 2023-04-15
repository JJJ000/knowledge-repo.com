---
title: A pattern that can be used to identify a period
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: The regular expression to match a dot in Python is simply a period symbol `.`.
---

**Contents**

[TOC]

## Introduction

Regular expressions are patterns of characters that are commonly used in text processing tasks such as search and replace, data extraction, and validation. They are implemented in various programming languages, including Python, and can be used to match specific character sequences, such as a dot.

In this article, we will discuss how to match a dot in Python using regular expressions.

## Matching a dot using a single character

The dot character (.) is a special metacharacter in regular expressions that matches any single character except newline (\n). Therefore, we can use a simple regular expression pattern of a single dot to match any occurrence of a dot in a string.

```python
import re

string = "The quick brown fox jumps over the lazy dog."

result = re.findall(".", string)

print(result)
```

Output
```
['T', 'h', 'e', ' ', 'q', 'u', 'i', 'c', 'k', ' ', 'b', 'r', 'o', 'w', 'n', ' ', 'f', 'o', 'x', ' ', 'j', 'u', 'm', 'p', 's', ' ', 'o', 'v', 'e', 'r', ' ', 't', 'h', 'e', ' ', 'l', 'a', 'z', 'y', ' ', 'd', 'o', 'g', '.']
```

As we can see from the output, the regular expression pattern "." has matched every occurrence of a single character in the string, including the dot.

## Escaping the dot character

Sometimes, we may want to match a literal dot character in a string and not the any single character metacharacter. In this case, we can escape the dot character using the backslash (\) character. The backslash tells the regular expression engine to treat the following character as a literal character and not a metacharacter.

```python
import re

string = "The quick brown fox jumps over the lazy dog."

result = re.findall("\.", string)

print(result)
```

Output
```
['.']
```

As we can see from the output, the regular expression pattern "\." has matched only the literal dot character in the string.

## Using character classes

Another way to match a dot character is by using character classes. Character classes are sets of characters enclosed in square brackets [] that match any single character that is a member of the set. The dot character can be included in a character class by placing it inside the square brackets.

```python
import re

string = "The quick brown fox jumps over the lazy dog."

result = re.findall("[.]", string)

print(result)
```

Output
```
['.']
```

As we can see from the output, the regular expression pattern "[.]" has matched only the literal dot character in the string.

## Conclusion

Matching a dot character in Python using regular expressions is a simple task, but it requires an understanding of regular expression metacharacters and their special meanings. By using the dot character, escaping it, or including it in a character class, we can match any dot character in a string or text.
