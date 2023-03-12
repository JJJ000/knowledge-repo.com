---
title: Substitute the initial incidence of a specific sequence of characters in python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: To replace the first occurrence of a string in Python, use the replace() method with the count parameter set to 1.
---

**Contents**

[TOC]

1. Introduction
Replacing the first occurrence of a string is a common task when working with strings in Python. There are several ways to accomplish this, each with its own advantages and disadvantages. In this article, we will explore three different methods for replacing the first occurrence of a string in Python.

2. Using replace() method with count parameter
The `replace()` method can be used to replace all occurrences of a string in a given string. However, if we pass count parameter as 1, it will replace only the first occurrence. Here is the code snippet:

```
string = "I like Python"
new_string = string.replace("like", "hate", 1)
print(new_string)
```

Output: `I hate Python`

In the above code, `replace()` method replaces the first occurrence of "like" with "hate" in the given string.

3. Using split() and join() methods
Another approach to replace the first occurrence of a string in Python is to use the `split()` and `join()` string methods. Here is the code snippet:

```
string = "I love Python"
old_word = "love"
new_word = "hate"
words = string.split(old_word, 1)
if len(words) == 2:
    new_string = new_word.join(words)
else:
    new_string = string
print(new_string)
```

Output: `I hate Python`

In the above code, the `split()` method is used to split the given string into two parts using the old_word as a delimiter. The second argument of `split()` method passed as 1, which means it will split the string into two parts at most using `old_word`. The `if` statement checks if the split resulted in two parts, which means `old_word` was found. Then the `join()` method is used to join the parts with the new_word.

4. Using regular expression
The `re` module provides a `sub()` function that can be used with regular expressions. We can use this to replace the first occurrence of a string. Here is the code snippet:

```
import re
string = "I like Python"
old_word = "like"
new_word = "hate"
new_string = re.sub(old_word, new_word, string, 1)
print(new_string)
```

Output: `I hate Python`

In the above code, the `sub()` method is used to replace the first occurrence of `old_word` with `new_word` in the given string. The fourth argument to the `sub()` method is the count parameter, which specifies the maximum number of replacements to be made. In this case, we have set it to 1, which means it will replace only the first occurrence.

5. Conclusion

These are three different methods of replacing the first occurrence of a string in Python. The easiest way is to use the `replace()` method with the count parameter. The second method is to use the `split()` and `join()` methods. Using a regular expression is the most flexible method, but it may not be the most performant for very large strings. Choose the method based on your specific needs and requirements.
