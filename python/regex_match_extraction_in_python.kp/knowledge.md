---
title: Retrieve a portion of a regular expression match
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the group() or group(n) method on the match object to extract a part of the regex match in Python, where n is the number of the capture group.
---

**Contents**

[TOC]

Introduction
In Python, we can use regular expressions or regex to search for patterns within strings. Regex allows us to search for specific characters, strings, or patterns in a text. We can use Python's built-in re module to perform regex operations.

One useful application of regex is to extract part of a match. If we have a regex that matches a specific pattern, we can use regex groups to extract specific parts of that pattern.

In this article, we will discuss how to extract part of a regex match in Python.

Section 1: Creating a regex pattern
To extract part of a regex match, we first need to create a regex pattern that matches the text we want to extract. We can use regex groups to specify which part of the pattern we want to extract.

Here's an example of a regex pattern that matches an email address:

```
import re

pattern = r'([\w\.-]+)@([\w\.-]+)(\.[\w\.]+)'
```

This pattern has three groups:

1. `([\w\.-]+)`: this group matches one or more alphanumeric characters, underscores, dots, and hyphens, which constitute the email username.
2. `@`: this matches the @ symbol that separates the username from the domain name.
3. `([\w\.-]+)(\.[\w\.]+)`: this group matches the domain name, which consists of two parts. The first part matches one or more alphanumeric characters, underscores, dots, and hyphens, followed by a dot. The second part matches one or more alphanumeric characters, dots, and hyphens.

Section 2: Using regex to extract part of a match
Once we have our regex pattern, we can use it to search for matches in a string. We can use the `re.search()` function to find the first match in a string.

Here's an example of how to extract the username and domain name from an email address using the regex pattern we created earlier:

```
email = 'johndoe@example.com'

match = re.search(pattern, email)

if match:
    username = match.group(1)
    domain = match.group(2) + match.group(3)
    
    print('Username:', username)
    print('Domain:', domain)
```

In this example, we first search for a match in the `email` string using the `re.search()` function. If a match is found, we extract the first and second group using the `group()` method, and concatenate the second and third group to get the complete domain name. Finally, we print out the username and domain name.

Section 3: Using named groups to extract part of a match
In addition to using numbered groups, we can also use named groups to extract specific parts of a match. Named groups are defined by enclosing a group with `(?P<name>...)`, where `name` is the name of the group.

Here's an example of a modified version of our email regex pattern that uses named groups:

```
pattern = r'(?P<username>[\w\.-]+)@(?P<domain>[\w\.-]+)(\.[\w\.]+)'
```

In this pattern, we replaced the numbered groups with named groups. We named the first group `username`, and the second group `domain`.

We can extract the named groups using the `group()` method with the name of the group as an argument:

```
email = 'johndoe@example.com'

match = re.search(pattern, email)

if match:
    username = match.group('username')
    domain = match.group('domain') + match.group(3)
    
    print('Username:', username)
    print('Domain:', domain)
```

In this example, we extract the `username` and `domain` named groups using the `group()` method with the group name as the argument. We then concatenate the second and third group to get the complete domain name.

Section 4: Conclusion
In this article, we discussed how to extract part of a regex match in Python. We saw how to create a regex pattern that matches the text we want to extract, how to use regex groups to extract specific parts of the pattern, and how to extract named groups. With these tools, we can easily extract and manipulate text that matches a specific pattern.
