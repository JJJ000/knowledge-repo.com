---
title: In python, divide a string using a separator
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: string.split(delimiter)  splits a string by a specified delimiter in python.
---

**Contents**

[TOC]

# Introduction

Python provides easy ways to split strings into a list of substrings based on a delimiter. A delimiter can be a character or a sequence of characters that are used to separate the original string into smaller parts. The `split()` method is the most commonly used function to split strings in Python.

In this article, we will explore different ways to split a string by a delimiter in Python.

# Using the split() method

The `split()` method is a built-in string method that returns a list of substrings after splitting the original string by the specified delimiter.

Here is the syntax of `split()` method:

```python
string.split(separator, maxsplit)
```

- `separator`: The character or sequence of characters to be used as the delimiter.
- `maxsplit`: An optional parameter that specifies the maximum number of splits to be performed. If not provided, all possible splits will be performed.

Let's split a string using the `split()` method:

```python
string = "apple,banana,orange"
fruits = string.split(",")
print(fruits)
```

Output:

```
['apple', 'banana', 'orange']
```

In the above example, we split the string `"apple,banana,orange"` using the comma `,` as the delimiter. The `split()` method returns a list of substrings `['apple', 'banana', 'orange']`.

# Using the split() method with whitespace delimiter

If no delimiter is specified in the `split()` method, it will use whitespace as the default delimiter and split the string into words.

Let's split a string using the `split()` method without specifying the separator:

```python
text = "Hello World! How are you?"
words = text.split()
print(words)
```

Output:

```
['Hello', 'World!', 'How', 'are', 'you?']
```

In the above example, we split the string `"Hello World! How are you?"` without specifying the separator. The `split()` method returns a list of words `['Hello', 'World!', 'How', 'are', 'you?']`.

# Using the partition() method

The `partition()` method is another string method that can be used to split the original string into three parts, before and after the specified separator.

Here is the syntax of `partition()` method:

```python
string.partition(separator)
```

- `separator`: The character or sequence of characters to be used as the delimiter.

Let's split a string using the `partition()` method:

```python
string = "apple,banana,orange"
first, sep, last = string.partition(",")
print(first)
print(last)
```

Output:

```
apple
banana,orange
```

In the above example, we split the string `"apple,banana,orange"` using the comma `,` as the delimiter. The `partition()` method returns a tuple of three substrings `"apple"`, `","` and `"banana,orange"`. We can then unpack this tuple into separate variables `first`, `sep`, and `last`.

# Using the rsplit() method

The `rsplit()` method is similar to the `split()` method, but it splits the string from right to left.

Here is the syntax of `rsplit()` method:

```python
string.rsplit(separator, maxsplit)
```

- `separator`: The character or sequence of characters to be used as the delimiter.
- `maxsplit`: An optional parameter that specifies the maximum number of splits to be performed. If not provided, all possible splits will be performed.

Let's split a string using the `rsplit()` method:

```python
string = "apple,banana,orange"
fruits = string.rsplit(",", 1)
print(fruits)
```

Output:

```
['apple,banana', 'orange']
```

In the above example, we split the string `"apple,banana,orange"` using the comma `,` as the delimiter and performed only `1` split from right to left. The `rsplit()` method returns a list of substrings `['apple,banana', 'orange']`.

# Conclusion

In this article, we explored different ways to split a string by a delimiter in Python. The `split()` method and `rsplit()` method are the most commonly used functions to split strings. The `partition()` method can also be used to split strings into three parts.
