---
title: Comparing the use of collections.emptylist() to creating a new instance of a list
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Collections.emptyList() returns an immutable empty list, while creating a new instance will create a modifiable list.
---

**Contents**

[TOC]

1. **Collections.emptyList()**
- Collections.emptyList() is a static factory method that returns an immutable empty List. It is a convenient way to create an empty List instance that won't be modified. This method is available since Java 1.4.

2. **Creating a new instance**
- Creating a new instance of a List is a more verbose approach to creating an empty List. It requires instantiating a new List and then adding elements to it. This approach is available since Java 1.0.
