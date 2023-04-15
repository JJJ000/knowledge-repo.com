---
title: Is there a more efficient way to split a string than using re.split("( )+") which leads to a result list with spaces?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Yes, you can use re.split() without any arguments to split the string by whitespace and remove multiple whitespaces at once.
---

**Contents**

[TOC]

Splitting a string with re.split("( )+") in Python

When splitting a string with Python's regular expression tool, it is sometimes necessary to split on multiple spaces rather than just one. One common approach is to use the re.split('( )+'), as shown below:

```python
import re
string = "Hello       world!     How are you?"
result = re.split('( )+',string)
print(result)
```

This results in the following output:

```
['Hello', '   ', 'world!', '     ', 'How', ' ', 'are', ' ', 'you?']
```


Section 1: The problem with re.split("( )+")

As can be seen from the output, the result list contains single spaces in addition to the split words. This is because the regular expression defines a group consisting of a single space, which is then repeated one or more times by the plus sign. Therefore, each group of spaces is kept as a separate item in the result list.

This can be inconvenient because it requires additional processing to remove the spaces, which can lead to code clutter and decreased readability.


Section 2: Using str.split() instead

An alternative approach to splitting a string on multiple spaces is to use the built-in str.split() method. This method splits a string into a list of substrings based on a specified separator. In our case, we can use the split() method with no arguments, which will split the string on any whitespace character (including both spaces and tabs) and return a list of non-empty substrings. Here is an example:

```python
string = "Hello       world!     How are you?"
result = string.split()
print(result)
```

This results in the following output:

```
['Hello', 'world!', 'How', 'are', 'you?']
```

As can be seen, the result list contains only the split words without any single spaces.


Section 3: Using re.split() with lookarounds

Another approach to splitting a string on multiple spaces is to use a regular expression with lookarounds. Lookarounds are zero-width assertions that match a pattern but do not consume any part of the string being searched. In our case, we can use a positive lookbehind to match any space that is preceded by a non-space character, and a positive lookahead to match any space that is followed by a non-space character. Here is an example:

```python
import re
string = "Hello       world!     How are you?"
result = re.split('(?<=\S) +(?=\S)', string)
print(result)
```

This results in the following output:

```
['Hello', 'world!', 'How', 'are', 'you?']
```

As can be seen, the result list contains only the split words without any single spaces. The regular expression consists of two lookarounds that match a space only if it is not preceded or followed by a space. The '\S' matches any non-space character.


Section 4: Conclusion

In conclusion, there are different approaches to splitting a string on multiple spaces in Python. While the re.split("( )+") approach is straightforward, it can result in a result list with single spaces that require additional processing. A simpler and cleaner approach is to use the split() method, which splits the string on any whitespace character and returns a list of non-empty substrings. Another approach is to use a regular expression with lookarounds to match spaces that are not surrounded by spaces. The choice of approach will depend on the specific requirements of the task at hand.
