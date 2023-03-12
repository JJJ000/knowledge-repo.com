---
title: Merging two lists while retaining all unique elements, without eliminating duplicate entries from the source list
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: To combine two lists and remove duplicates, use the set() function and convert the resulting set back into a list, but do not modify the original lists to preserve the duplicates.
---

**Contents**

[TOC]

## Section 1: List combination and duplicate removal

To combine two lists and remove duplicates, we can use the `set()` function along with the union operator `|`. Here's an example:

```python
list1 = [1, 2, 3]
list2 = [2, 3, 4]
combined_list = list(set(list1) | set(list2))
```

In this example, `set(list1)` and `set(list2)` create sets from the original lists, which automatically removes duplicates. The `|` operator performs a union operation, which combines the two sets and removes any duplicates. Finally, `list()` is used to convert the set back to a list.

After running this code, `combined_list` will be `[1, 2, 3, 4]`.

## Section 2: Removing duplicates only from combined list

If we want to remove duplicates only from the combined list, without modifying the original lists, we can use slice notation to create a new list with only unique elements. Here's how:

```python
list1 = [1, 2, 3]
list2 = [2, 3, 4]
combined_list = list1 + list2
unique_list = []
for element in combined_list:
    if element not in unique_list:
        unique_list.append(element)
```

In this example, `combined_list` is created by concatenating `list1` and `list2`. Then, a new list called `unique_list` is created to hold only the unique elements. The `for` loop iterates over each element in `combined_list`, and checks if it is already in `unique_list` using the `not in` operator. If the element is not already in the list, it is appended using the `append()` method. 

After running this code, `unique_list` will be `[1, 2, 3, 4]`, but the original `list1` and `list2` will remain unchanged.


## Section 3: Using a set to remove duplicates only from combined list

Another way to remove duplicates only from the combined list is to use a set, but convert it back to a list afterwards. Here's how:

```python
list1 = [1, 2, 3]
list2 = [2, 3, 4]
combined_list = list1 + list2
unique_set = set(combined_list)
unique_list = list(unique_set)
```

In this example, `combined_list` is created by concatenating `list1` and `list2`. Then, a new set called `unique_set` is created by passing `combined_list` as an argument to the `set()` function. This automatically removes duplicates. Finally, `unique_set` is converted back to a list by passing it as an argument to the `list()` function.

After running this code, `unique_list` will be `[1, 2, 3, 4]`, but the original `list1` and `list2` will remain unchanged.


## Section 4: Conclusion

There are multiple ways to combine two lists and remove duplicates in Python. The easiest way is to use `set()` and the union operator `|` to create a new list with only unique elements. Alternatively, we can use slice notation to extract unique elements from a combined list, or use a set to automatically remove duplicates and convert it back to a list. It's important to note that the original lists need not be modified in any of these cases.
