---
title: Verify whether a term is present within a sequence of characters using python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-06 00:00:00
updated_at: 2023-03-06 00:00:00
tldr: Use the `in` keyword to check if a word is in a string in Python `word` in string.
---

**Contents**

[TOC]

## Using the `in` keyword

The easiest way to check if a word is in a string is to use the `in` keyword. This method simply checks if the word is a substring of the string you are searching in.

Here's an example:

```python
string = "The quick brown fox jumps over the lazy dog"
word = "fox"
 
if word in string:
    print(f"'{word}' found in '{string}'")
else:
    print(f"'{word}' not found in '{string}'")
```

Output:
```
'fox' found in 'The quick brown fox jumps over the lazy dog'
```


## Using the `find()` method

The `find()` method returns the index of the first occurrence of the substring in the given string. If the substring is not found, it returns -1.

Here's an example:

```python
string = "The quick brown fox jumps over the lazy dog"
word = "fox"
 
if string.find(word) != -1:
    print(f"'{word}' found in '{string}'")
else:
    print(f"'{word}' not found in '{string}'")
```

Output:
```
'fox' found in 'The quick brown fox jumps over the lazy dog'
```


## Using regular expressions

If you need more advanced pattern matching, you can use regular expressions. This method requires the `re` module.

Here's an example using `re.search()`:

```python
import re

string = "The quick brown fox jumps over the lazy dog"
word = "fox"
 
if re.search(word, string):
    print(f"'{word}' found in '{string}'")
else:
    print(f"'{word}' not found in '{string}'")
```

Output:
```
'fox' found in 'The quick brown fox jumps over the lazy dog'
```


## Conclusion

All three methods achieve the same result, but using the `in` keyword is the simplest and most concise way to check if a word is in a string. However, the other methods can be useful if you need to perform more advanced pattern matching.
