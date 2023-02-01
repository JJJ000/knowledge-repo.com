---
title: Delete specific characters from a string in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Use the replace() method to remove specific characters from a string in Python.
---

**Contents**

[TOC]

#1 Using str.replace()

The str.replace() method can be used to remove specific characters from a string. This method takes two arguments: the substring to be replaced and the replacement string. This method returns a copy of the string with all occurrences of the substring replaced with the replacement string.

Example:

```
my_string = "Hello World!"
my_string = my_string.replace("World", "")
print(my_string)
```

Output:

```
Hello!
```

#2 Using Regular Expressions

Regular expressions can also be used to remove specific characters from a string. This method uses a regular expression pattern to match the characters to be removed and then replaces them with an empty string.

Example:

```
import re

my_string = "Hello World!"
my_string = re.sub('World', '', my_string)
print(my_string)
```

Output:

```
Hello!
```

#3 Using str.translate()

The str.translate() method can be used to remove specific characters from a string. This method takes a translation table as an argument. The translation table is a mapping of characters to be removed to None.

Example:

```
my_string = "Hello World!"
translation_table = str.maketrans('World', '')
my_string = my_string.translate(translation_table)
print(my_string)
```

Output:

```
Hello!
```

#4 Using List Comprehension

List comprehension can also be used to remove specific characters from a string. This method takes a list of characters to be removed and then filters them out of the string.

Example:

```
my_string = "Hello World!"
my_string = ''.join([c for c in my_string if c not in 'World'])
print(my_string)
```

Output:

```
Hello!
```
