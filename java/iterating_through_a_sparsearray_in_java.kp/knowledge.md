---
title: What is the best way to loop through a sparsearray?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use a for loop to iterate through the elements of the SparseArray.
---

**Contents**

[TOC]

### Iterating Through a SparseArray

1. Create a `SparseArray` object and populate it with data.

```java
SparseArray<String> sparseArray = new SparseArray<>();
sparseArray.put(1, "foo");
sparseArray.put(2, "bar");
sparseArray.put(4, "baz");
```

2. Use the `keySet()` method of the `SparseArray` object to get a `Set` of all the keys in the `SparseArray` object.

```java
Set<Integer> keys = sparseArray.keySet();
```

3. Iterate through the `Set` of keys using a `for` loop.

```java
for (Integer key : keys) {
    String value = sparseArray.get(key);
    System.out.println("key: " + key + ", value: " + value);
}
```

4. Output the key and value of each entry in the `SparseArray` object.

```
key: 1, value: foo
key: 2, value: bar
key: 4, value: baz
```
