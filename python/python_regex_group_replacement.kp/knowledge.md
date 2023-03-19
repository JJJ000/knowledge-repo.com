---
title: Replacing groups with Python regex happens instantly
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: One can use the regular expression replacement syntax to replace captured groups instantly in Python regex.
---

**Contents**

[TOC]

Introduction to Python Regex and Group Replacement

Python's regex library is a powerful tool that allows developers to search, match, and manipulate text. One of the most useful features of regex is the ability to replace text based on patterns.

In addition to simple text replacement, Python regex allows for more advanced manipulation by using groups. These groups work like variables, allowing you to capture specific portions of your text and reuse them in your replacement.

In this article, we'll explore how to use Python regex to instantly replace groups.

Step 1: Capturing Groups in Python Regex

Groups are identified by using parentheses in your regex pattern. For example, the following regex pattern has two groups: one that captures a person's first name, and one that captures their last name.

```
import re

name_pattern = re.compile(r'(\w+)\s(\w+)')
```

In this pattern, the `\w+` expression matches one or more word characters (i.e., letters, digits, and underscores). The `\s` expression matches a single whitespace character.

To capture these groups and use them for replacement, we can use the backslash symbol followed by the group number. For example, if we want to swap the first and last names, we can use the following replacement string:

```
output = re.sub(name_pattern, r'\2 \1', input_text)
```

In this example, we're using `\2` to refer to the second captured group (i.e., the last name) and `\1` to refer to the first captured group (i.e., the first name).

Step 2: Using Functions to Replace Groups

Python regex also allows for more advanced group replacement using functions. To use a function, we pass a callable object as the second argument to the `re.sub()` function.

This callable object should take a single argument, which is a `Match` object containing information about the match. The function should return the replacement string.

For example, let's say we want to capitalize the first letter of each word in a sentence. We can use the following regex pattern to match each word:

```
import re

word_pattern = re.compile(r'\b\w')
```

In this pattern, the `\b` expression matches a word boundary, and `\w` matches a single word character.

To capitalize the first letter of each word, we can define a function that takes a match object and returns the matched text with the first letter capitalized:

```
def capitalize(match):
    return match.group(0).upper()
```

We can then use this function with `re.sub()` to capitalize the first letter of each word:

```
input_text = 'hello world'
output = re.sub(word_pattern, capitalize, input_text)
```

In this example, the `capitalize()` function is called for each match of the `word_pattern` regex. The function returns the matched text with the first letter capitalized, which is used as the replacement.

Step 3: Using Named Groups

Finally, we can make our code more readable and maintainable by using named groups. Named groups are identified by using `(?P<name>...)` syntax in your regex pattern.

For example, let's say we want to match dates in the format `mm/dd/yyyy`. We can use the following regex pattern with named groups to capture each part of the date:

```
import re

date_pattern = re.compile(r'(?P<month>\d{2})/(?P<day>\d{2})/(?P<year>\d{4})')
```

In this pattern, we're using named groups to capture the month, day, and year parts of the date. We can then refer to these groups by name in our replacement string:

```
output = re.sub(date_pattern, r'\g<day>-\g<month>-\g<year>', input_text)
```

In this example, we're using the `\g<name>` syntax to refer to the named groups in our replacement string.

Conclusion

In conclusion, Python regex provides powerful pattern matching and group replacement functionality. By using capturing groups, functions, and named groups, we can manipulate text in a variety of ways to suit our needs.
