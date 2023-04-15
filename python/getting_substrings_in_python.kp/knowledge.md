---
title: What is the syntax for extracting a substring from a string in python?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can use the slicing syntax (string[startend]) to get a substring of a string in Python.
---

**Contents**

[TOC]

**Using the Slice Notation**

The slice notation is a very powerful tool for extracting substrings. It is a special syntax used for selecting a range of characters within a string. It takes the form `string[start:stop:step]`, where `start` is the starting index, `stop` is the stopping index, and `step` is the increment between indices.

**Example**

Let's say we have the string `"Hello World!"` and we want to get the substring `"llo Wo"`. We can use the slice notation to do this:

```
string = "Hello World!"
substring = string[2:8:1]
print(substring)
```

The output of this code will be `llo Wo`.

**Using the `split` Method**

The `split` method is another way of getting a substring from a string. It takes a delimiter as an argument and returns a list of strings split by the delimiter.

**Example**

Let's say we have the string `"Hello World!"` and we want to get the substring `"llo Wo"`. We can use the `split` method to do this:

```
string = "Hello World!"
substring = string.split(' ')[1]
print(substring)
```

The output of this code will be `llo Wo`.

**Using the `find` Method**

The `find` method is a third way of getting a substring from a string. It takes a substring as an argument and returns the starting index of the substring in the string.

**Example**

Let's say we have the string `"Hello World!"` and we want to get the substring `"llo Wo"`. We can use the `find` method to do this:

```
string = "Hello World!"
start_index = string.find("llo Wo")
end_index = start_index + len("llo Wo")
substring = string[start_index:end_index]
print(substring)
```

The output of this code will be `llo Wo`.
