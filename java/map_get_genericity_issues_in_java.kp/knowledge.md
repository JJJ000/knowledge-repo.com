---
title: What are the limitations of map.get(object key) in terms of genericity?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Map.get(Object key) is not fully generic in Java because it requires an exact type match between the key and the value.
---

**Contents**

[TOC]

1. Type Erasure:
------------------------
Map.get() is not fully generic in Java due to type erasure. When a generic type is compiled, all of the type information is removed and replaced with a single type, usually Object. This means that the compiler will not be able to determine the type of the key that is passed in to the Map.get() method, and thus will not be able to return the correct type of value.

2. Raw Types:
------------------------
Another reason why Map.get() is not fully generic in Java is due to the use of raw types. Raw types are used when a type parameter is not specified, which can lead to unexpected results. For example, if a Map is declared with a raw type, the compiler will not be able to determine the type of the key that is passed in to the Map.get() method, and thus will not be able to return the correct type of value.

3. Type Mismatch:
------------------------
The third reason why Map.get() is not fully generic in Java is due to type mismatch. If the type of the key that is passed in to the Map.get() method does not match the type of the key that is stored in the Map, then the compiler will not be able to return the correct type of value.

4. Unchecked Casts:
------------------------
Finally, Map.get() is not fully generic in Java due to the use of unchecked casts. Unchecked casts are used when a type parameter is not specified, which can lead to unexpected results. For example, if a Map is declared with an unchecked cast, then the compiler will not be able to determine the type of the key that is passed in to the Map.get() method, and thus will not be able to return the correct type of value.
