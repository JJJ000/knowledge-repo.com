---
title: Remove all elements that are not 0 from the list
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the list comprehension approach to create a new list with only non-None values, but excluding 0 values by adding an if-statement to the expression.
---

**Contents**

[TOC]

### Using List Comprehension

The following code can be used to remove None values from a list without removing the 0 value:

```
lst = [0, None, 1, 2, None, 3, None, 4]

filtered_lst = [x for x in lst if x is not None]

print(filtered_lst)
```

Output:
```
[0, 1, 2, 3, 4]
```

### Using Filter() Method

The following code can be used to remove None values from a list without removing the 0 value:

```
lst = [0, None, 1, 2, None, 3, None, 4]

filtered_lst = list(filter(lambda x: x is not None, lst))

print(filtered_lst)
```

Output:
```
[0, 1, 2, 3, 4]
```

### Using List Iteration

The following code can be used to remove None values from a list without removing the 0 value:

```
lst = [0, None, 1, 2, None, 3, None, 4]

filtered_lst = []

for x in lst:
    if x is not None:
        filtered_lst.append(x)

print(filtered_lst)
```

Output:
```
[0, 1, 2, 3, 4]
```

### Using Remove() Method

The following code can be used to remove None values from a list without removing the 0 value:

```
lst = [0, None, 1, 2, None, 3, None, 4]

for x in lst:
    if x is None:
        lst.remove(x)

print(lst)
```

Output:
```
[0, 1, 2, 3, 4]
```
