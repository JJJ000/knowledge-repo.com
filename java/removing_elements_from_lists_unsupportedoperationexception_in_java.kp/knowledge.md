---
title: What causes an unsupportedoperationexception when attempting to remove an element from a list?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The UnsupportedOperationException is thrown when trying to remove an element from an unmodifiable List.
---

**Contents**

[TOC]

### Explanation
UnsupportedOperationException is thrown when an application attempts to perform an operation that is not supported by the class or interface. This is usually the case when attempting to modify an unmodifiable collection, such as an immutable list.

### Causes 
This exception is thrown when an application attempts to remove an element from an unmodifiable list. Unmodifiable lists are those that cannot be modified, such as the ones created by the Collections.unmodifiableList() method. 

### Solution
The best way to avoid this exception is to use a modifiable list instead of an unmodifiable list. If you must use an unmodifiable list, you can use the List.set() method to replace elements in the list.
