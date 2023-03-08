---
title: In what situations should %r be preferred over %s in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: %r is used for debugging and %s is used for displaying to users.
---

**Contents**

[TOC]

### Introduction

Python provides a powerful formatting mechanism through the use of the `%` operator, which is used to substitute values of variables or expressions into strings. When using this operator with strings, there are two main placeholders that can be used to represent textual data, `%s` and `%r`. Although the two placeholders appear to be similar, they have different use cases, and in this article, we'll explore when to use `%r` instead of `%s`.

### %s Placeholder

The `%s` placeholder is used to format strings in a way that is friendly to humans. It will convert any non-string values to strings using the `str()` function, and then substitute the resulting string in place of the placeholder. Here's an example:

```
name = 'John'
age = 25
text = 'My name is %s and I am %s years old.' % (name, age)
print(text)
# Output: My name is John and I am 25 years old.
```

In this example, the `%s` placeholders are replaced by the values of `name` and `age`, which have been converted to strings before being substituted.

### %r Placeholder

The `%r` placeholder, on the other hand, is used to format strings in a way that is friendly to the Python interpreter. It will convert any non-string values to strings using the `repr()` function, which returns a string that is formatted in a way that is valid Python code. Here's an example:

```
name = 'John'
age = 25
text = 'My name is %r and I am %r years old.' % (name, age)
print(text)
# Output: My name is 'John' and I am 25 years old.
```

In this example, the `%r` placeholders are replaced by the values of `name` and `age`, which have been converted to strings using `repr()`, resulting in a string that includes quotes around the name.

### When to Use %r

There are a few cases where using `%r` instead of `%s` can be beneficial:

1. Debugging - When debugging, it can be useful to see the exact value of a variable, even if it includes non-printable characters or other special characters that wouldn't be friendly to humans.

2. Representation - When working with objects that have a `__repr__()` method, it can be useful to use `%r` to obtain a string representation of the object that can be used to recreate it later.

3. Ambiguous Data - When working with data that is ambiguous or poorly formatted, using `%r` can help prevent errors by returning a string that is valid Python code.

In general, it's a good idea to use `%s` when formatting strings for display to the user, and `%r` when formatting strings for consumption by the Python interpreter.

### Conclusion

In this article, we've explored the differences between the `%s` and `%r` placeholders when formatting strings in Python. While `%s` is used to format strings in a way that is friendly to humans, `%r` is used to format strings in a way that is friendly to the Python interpreter. By understanding the differences between these two placeholders, you can choose the appropriate one for your use case and avoid common formatting errors.
