---
title: Delete the final three characters in a sequence
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use string slicing to remove the last three characters of a string in Python, like this string[-3].
---

**Contents**

[TOC]

# String slicing method
One way to remove the last 3 characters of a string is to use string slicing. We can slice the string from the start to the third-last character using `[:-3]` notation. Here's an example:

```
string = "hello world"
new_string = string[:-3]
print(new_string)  # Output: "hello wo"
```

In this example, `new_string` will have the value `"hello wo"` since we removed the last three characters `"rld"` using string slicing.

# Using the string[:-3] method
Another way to remove the last 3 characters of a string is to use the same string slicing method, but wrapped in a function. Here's an example:

```
def remove_last_3_chars(string):
    return string[:-3]

string = "hello world"
new_string = remove_last_3_chars(string)
print(new_string)  # Output: "hello wo"
```

In this example, we defined a function `remove_last_3_chars` that takes a string as an argument and returns a new string with the last three characters removed. We then used this function to remove the last three characters from the string `"hello world"`.

# Using the rstrip() method
A third way to remove the last 3 characters of a string is to use the built-in `rstrip()` method. We can pass in the characters we want to remove as an argument. Here's an example:

```
string = "hello world"
new_string = string.rstrip("rld")
print(new_string)  # Output: "hello wo"
```

In this example, we used the `rstrip()` method to remove the characters `"rld"` from the end of the string `"hello world"`. The resulting string is `"hello wo"`.

# Using the replace() method
A fourth way to remove the last 3 characters of a string is to use the built-in `replace()` method. We can replace the last three characters with an empty string `""`. Here's an example:

```
string = "hello world"
new_string = string.replace("rld", "")
print(new_string)  # Output: "hello wo"
```

In this example, we used the `replace()` method to remove the characters `"rld"` from the end of the string `"hello world"`. The resulting string is `"hello wo"`.
