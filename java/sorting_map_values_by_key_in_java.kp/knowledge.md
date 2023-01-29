---
title: What is the most efficient way to order map values by key in java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: You can sort Map values by key in Java using the Map.Entry.comparingByKey() method.
---

**Contents**

[TOC]

### Solution 1: Using TreeMap

TreeMap is a Red-Black tree based implementation of Map which keeps the entries sorted according to the natural ordering of its key.

1. Create a TreeMap object:

```java
TreeMap<String, Integer> map = new TreeMap<String, Integer>();
```

2. Add entries to the TreeMap object:

```java
map.put("Key1", 10);
map.put("Key2", 20);
map.put("Key3", 30);
```

3. Print the sorted entries:

```java
for (Map.Entry<String, Integer> entry : map.entrySet()) {
    System.out.println(entry.getKey() + " : " + entry.getValue());
}
```

### Solution 2: Using Comparator

1. Create a Comparator object:

```java
Comparator<String> comparator = new Comparator<String>() {
    public int compare(String s1, String s2) {
        return s1.compareTo(s2);
    }
};
```

2. Create a TreeMap object:

```java
TreeMap<String, Integer> map = new TreeMap<String, Integer>(comparator);
```

3. Add entries to the TreeMap object:

```java
map.put("Key1", 10);
map.put("Key2", 20);
map.put("Key3", 30);
```

4. Print the sorted entries:

```java
for (Map.Entry<String, Integer> entry : map.entrySet()) {
    System.out.println(entry.getKey() + " : " + entry.getValue());
}
```
