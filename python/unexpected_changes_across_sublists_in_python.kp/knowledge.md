---
title: Unexpected changes to the items in the lists of lists are being seen in the sublists
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: When a list of lists is modified, the changes can be reflected across all sublists, even if the modification was not intended.
---

**Contents**

[TOC]

# Section 1: Overview

When working with lists of lists in Python, it is important to be aware of the fact that changes to a single list may be reflected across all sublists. This can be a surprising behavior, as the changes may not be immediately apparent.

# Section 2: Causes

This behavior is caused by the fact that Python stores lists as references, rather than as copies. This means that when a list is created, Python stores the reference to the list in memory, rather than a copy of the list itself. Therefore, when a change is made to a single list, it is reflected across all sublists, as they all point to the same reference.

# Section 3: Examples

For example, consider the following code:

```
my_list = [[1, 2, 3], [4, 5, 6]]
my_list[0][0] = 9
print(my_list)
```

The output of this code will be `[[9, 2, 3], [4, 5, 6]]`, as the change to the first element of the first sublist is reflected across all sublists.

# Section 4: Solutions

In order to avoid this behavior, one must create copies of the list instead of references. This can be done using the `copy` module, as follows:

```
import copy
my_list = [[1, 2, 3], [4, 5, 6]]
my_list2 = copy.deepcopy(my_list)
my_list2[0][0] = 9
print(my_list)
```

The output of this code will be `[[1, 2, 3], [4, 5, 6]],` as the change to the first element of the first sublist is not reflected across all sublists.
