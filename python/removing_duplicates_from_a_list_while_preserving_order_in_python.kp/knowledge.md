---
title: What is the most efficient way to remove duplicates from a list while keeping the original order?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Use the `collections.OrderedDict` to remove duplicates while preserving order.
---

**Contents**

[TOC]

### Using Set
1. Create a set from the list. This will automatically remove any duplicates.
2. Convert the set back to a list.

### Using Loop
1. Create an empty list.
2. Iterate through the original list.
3. For each element in the list, check if it is already in the new list.
4. If it is not, append it to the new list.
5. Return the new list.
