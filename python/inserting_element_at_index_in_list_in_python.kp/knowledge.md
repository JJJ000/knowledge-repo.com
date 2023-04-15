---
title: Add an item at a particular index within a list and provide the revised version of the list
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the insert() method to insert an element at a specific index in a list and return the updated list.
---

**Contents**

[TOC]

Creating a list
---
Before we can insert an element at a specific index in a list, we first need to create a list. We can do this in Python by enclosing a sequence of elements in square brackets [ ]. For example, we can create a list of integers like this:

```python
numbers = [1, 2, 3, 4, 5]
```

Inserting an element at a specific index
---
To insert an element at a specific index in a list, we can use the insert() method. This method takes two arguments: the index at which to insert the element, and the element itself. For example, if we want to insert the number 6 at index 3 in the list above, we can do this:

```python
numbers.insert(3, 6)
```

This will insert the number 6 at index 3, shifting all the elements after that index to the right by one position.

Returning the updated list
---
To return the updated list, we can simply print it or store it in a variable. For example, we can print the updated list like this:

```python
print(numbers)
```

This will output the following:

```python
[1, 2, 3, 6, 4, 5]
```

Alternatively, we can store the updated list in a new variable like this:

```python
new_numbers = numbers.insert(3, 6)
```

Note that when using the insert() method, it modifies the original list in place and does not return a new list. So the above code will actually store None in the variable new_numbers, because the insert() method returns None. If you want to create a new list that is a copy of the original list with the element inserted at the specific index, you can use list slicing like this:

```python
new_numbers = numbers[:3] + [6] + numbers[3:]
```

This will create a new list that is a copy of the original list with the number 6 inserted at index 3, and store it in the variable new_numbers.
