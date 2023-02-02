---
title: What is the best way to arrange a list of strings in order?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: You can sort a list of strings in Python by using the built-in sorted() function.
---

**Contents**

[TOC]

# Using the sorted() Function 
The sorted() function can be used to sort a list of strings in Python.

Syntax:
```
sorted(list_of_strings)
```

Example:

```
list_of_strings = ["Apple", "Banana", "Mango", "Orange"]
sorted_list_of_strings = sorted(list_of_strings)

print(sorted_list_of_strings)

# Output: ['Apple', 'Banana', 'Mango', 'Orange']
```

# Using the sort() Method
The sort() method can be used to sort a list of strings in Python.

Syntax:
```
list_of_strings.sort()
```

Example:

```
list_of_strings = ["Apple", "Banana", "Mango", "Orange"]
list_of_strings.sort()

print(list_of_strings)

# Output: ['Apple', 'Banana', 'Mango', 'Orange']
```

# Using the sorted() Function with the reverse Parameter
The sorted() function can be used to sort a list of strings in reverse order by using the reverse parameter.

Syntax:
```
sorted(list_of_strings, reverse=True)
```

Example:

```
list_of_strings = ["Apple", "Banana", "Mango", "Orange"]
sorted_list_of_strings = sorted(list_of_strings, reverse=True)

print(sorted_list_of_strings)

# Output: ['Orange', 'Mango', 'Banana', 'Apple']
```

# Using the sort() Method with the reverse Parameter
The sort() method can be used to sort a list of strings in reverse order by using the reverse parameter.

Syntax:
```
list_of_strings.sort(reverse=True)
```

Example:

```
list_of_strings = ["Apple", "Banana", "Mango", "Orange"]
list_of_strings.sort(reverse=True)

print(list_of_strings)

# Output: ['Orange', 'Mango', 'Banana', 'Apple']
```
