---
title: Regular expressions in Python can produce a boolean output of either true or false
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Python regular expressions return a Boolean value of True or False depending on whether the pattern matches the given string or not.
---

**Contents**

[TOC]

Python Regular Expressions

Regular expressions, also known as regex, is a special sequence of characters that helps in pattern matching and finding matches in strings. In Python, the `re` module is used to work with regular expressions.

Matching with Regular Expressions

The `re.match()` method is used to match a pattern from the beginning of a string. It returns a match object if the pattern is found else it returns `None`.

```python
import re

string = "Python is a great language"
match_object = re.match(r"Python", string)

if match_object:
    print("Match found!")
else:
    print("Match not found!")
```

Output:
```
Match found!
```

Search with Regular Expressions

The `re.search()` method is used to search for a pattern anywhere in the string. It returns a match object if the pattern is found else it returns `None`.

```python
import re

string = "Python is a great language"
match_object = re.search(r"great", string)

if match_object:
    print("Match found!")
else:
    print("Match not found!")
```

Output:
```
Match found!
```

Returning True/False with Regular Expressions

Both `re.match()` and `re.search()` methods return a match object or `None`. To check if a pattern is found or not, we can use the `if` statement to check if the match object is truthy.

```python
import re

string = "Python is a great language"
match_object = re.search(r"Java", string)

if match_object:
    print("Match found!")
else:
    print("Match not found!")
```

Output:
```
Match not found!
```

Here, the `re.search()` method could not find a match for the pattern "Java" in the string "Python is a great language" and thus, returns `None`. The `if` statement checks if `None` is truthy or falsy and in this case, it is falsy, thus printing "Match not found!".
