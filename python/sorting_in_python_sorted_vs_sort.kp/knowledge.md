---
title: Can you explain the dissimilarities of "sorted(list)" and "list.sort()"?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: `sorted(list)` returns a new sorted list while `list.sort()` sorts the list in-place without returning anything.
---

**Contents**

[TOC]

Section 1: Definition

`sorted(list)` and `list.sort()` are both Python functions used to sort a list, but they have different methods of implementation and return different values.

Section 2: Method of implementation

`sorted(list)` creates a new sorted list and returns the sorted list, leaving the original list unchanged. This is known as a non-destructive method of implementation.

`list.sort()` sorts the list in place (i.e., modifies the original list) and returns `None`. This is a destructive method of implementation.

Section 3: Return values

`sorted(list)` returns a new sorted list, leaving the original list unchanged. This allows for chains of operations on a list without altering it.

`list.sort()` modifies the original list and returns `None`. This can be useful when you want to modify the list in place and do not need the original unsorted list.

Section 4: Time and space complexity

`sorted(list)` has a time complexity of O(n log n) and a space complexity of O(n).

`list.sort()` has a time complexity of O(n log n) and a space complexity of O(1) because it uses an in-place sorting algorithm. 

Overall, the differences between `sorted(list)` and `list.sort()` boil down to their method of implementation and return values. `sorted(list)` returns a new sorted list while leaving the original list unchanged, whereas `list.sort()` sorts the list in place and returns `None`. The time and space complexity of both functions are the same, except that `list.sort()` uses an in-place sorting algorithm, making it more memory efficient.
