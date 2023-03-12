---
title: What is the reason for receiving empty strings in split() outcomes?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Empty strings are returned in split() results in Python when there are consecutive delimiters, such as multiple spaces or commas in a row.
---

**Contents**

[TOC]

Section 1: Definition of split() function in Python
The split() function is a built-in string method that splits a string into a list of substrings based on a separator. The separator can be any character or sequence of characters. If no separator is provided, Python assumes a whitespace character as the separator.

Section 2: Cases when empty strings are returned in split() function results
When the separator appears at the beginning or the end of the string, it will create empty strings in the resulting list. For example, consider the following code:

```python
my_string = "one-two-three-"
result = my_string.split("-")
print(result)
```

This will output:
```python
['one', 'two', 'three', '']
```

As we can see, the empty string is present at the end of the list because the separator "-" appears at the end of the string.

Another scenario where empty strings can appear is when there are consecutive separators in the string. For instance:

```python
my_string = "one--two--three"
result = my_string.split("--")
print(result)
```

This would output:
```python
['one', '', 'two', '', 'three']
```

As we see, there are two empty strings in the resulting list. 

Section 3: Handling empty strings in split() function results
When empty strings are not desirable, we can filter them out using a conditional list comprehension like this:

```python
my_string = "one--two--three"
result = [s for s in my_string.split("--") if s]
print(result)
```

This will output:
```python
['one', 'two', 'three']
```

As we can see, we have removed all empty strings.

Section 4: Conclusion
In summary, empty strings are returned in split() function results when the separator appears at the beginning or the end of the string, or when there are consecutive separators in the string. To handle empty strings, we can filter them out using a conditional list comprehension.
