---
title: What is the process for replacing multiple parts of a string?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: Use the replace() method to replace multiple substrings of a string in Python.
---

**Contents**

[TOC]

## Using str.replace()

The `str.replace()` method can be used to replace multiple substrings of a string. It takes two arguments, the substring to be replaced and the substring to replace it with. The syntax for using `str.replace()` is as follows:

```python
string_name.replace("substring_to_replace", "replacement_substring")
```

For example, if we want to replace the substrings "Python" and "programming" with "Java" and "coding" respectively in the string "I love Python programming", we can use the following code:

```python
string = "I love Python programming"
string = string.replace("Python", "Java")
string = string.replace("programming", "coding")
print(string)
```

The output of the above code will be:

`I love Java coding`

## Using re.sub()

The `re.sub()` method can also be used to replace multiple substrings of a string. It takes three arguments, the substring to be replaced, the substring to replace it with, and the string in which the replacements are to be made. The syntax for using `re.sub()` is as follows:

```python
re.sub("substring_to_replace", "replacement_substring", string_name)
```

For example, if we want to replace the substrings "Python" and "programming" with "Java" and "coding" respectively in the string "I love Python programming", we can use the following code:

```python
import re
string = "I love Python programming"
string = re.sub("Python", "Java", string)
string = re.sub("programming", "coding", string)
print(string)
```

The output of the above code will be:

`I love Java coding`

## Using re.subn()

The `re.subn()` method can also be used to replace multiple substrings of a string. It takes three arguments, the substring to be replaced, the substring to replace it with, and the string in which the replacements are to be made. The syntax for using `re.subn()` is as follows:

```python
re.subn("substring_to_replace", "replacement_substring", string_name)
```

For example, if we want to replace the substrings "Python" and "programming" with "Java" and "coding" respectively in the string "I love Python programming", we can use the following code:

```python
import re
string = "I love Python programming"
string = re.subn("Python", "Java", string)
string = re.subn("programming", "coding", string)
print(string)
```

The output of the above code will be a tuple containing the replaced string and the number of replacements made:

`('I love Java coding', 2)`
