---
title: What is the distinction between using the '+=' operator and the extend() method when combining two lists?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: `+=` is used to concatenate two lists in-place, while extend() is used to add the elements of one list to the end of another list.
---

**Contents**

[TOC]

#### '+=' 
The '+=' operator is an augmented assignment operator which can be used to concatenate two lists. It takes the first list, adds the second list to it, and assigns the result to the first list. 

#### extend()
The extend() method is a built-in method which is used to add elements from one list to another. Unlike the '+=' operator, extend() adds each element from the second list to the end of the first list, rather than adding the second list as a whole.

#### Difference
The main difference between the '+=' operator and the extend() method is that '+=' adds the second list to the first list as a whole, while extend() adds each element from the second list to the end of the first list. Additionally, the '+=' operator is an augmented assignment operator, which means that it assigns the result of the operation to the first list, while the extend() method does not assign the result to the list.
