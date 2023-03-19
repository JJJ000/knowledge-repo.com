---
title: In python, what is the process for arranging the letters within a string in alphabetical order?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Use the sorted() function with the string as argument to sort the letters alphabetically.
---

**Contents**

[TOC]

Section 1: Introduction
One useful operation we may need to perform when working with strings in Python is sorting its letters in alphabetical order. This can be helpful for tasks such as identifying if two strings have the same letters regardless of order. In this guide, we will go through how to sort the letters in a string alphabetically in Python.

Section 2: Using sorted() function
One straightforward way to sort the letters in a string alphabetically is by utilizing Python's built-in `sorted()` function. We can convert our string to a list of characters, sort them in alphabetical order, and then join them back into a string. Here's an example:

```python
string = "hello world"
sorted_chars = sorted(string)
sorted_string = ''.join(sorted_chars)
print(sorted_string)
```

Output: 

```
dehllloorw
```

As we can see, the letters in the original string have been sorted in alphabetical order.

Section 3: Using .sort() method
If we don't need to preserve the original string and instead want to modify it directly, we can use the `.sort()` method of a list. We can first convert the string into a list of its characters, sort them, and then join them back into a string. Here's an example:

```python
string = "hello world"
char_list = list(string)
char_list.sort()
sorted_string = ''.join(char_list)
print(sorted_string)
```

Output:

```
dehllloorw
```

Again, the letters in our original string have been sorted alphabetically.

Section 4: Conclusion
Sorting the letters in a string alphabetically in Python can be achieved through various methods. We can use the `sorted()` function to return a new sorted string or utilize the `.sort()` method to modify the existing string. These techniques can be helpful in various scenarios when working with strings.
