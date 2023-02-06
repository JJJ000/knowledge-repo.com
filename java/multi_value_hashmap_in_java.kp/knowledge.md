---
title: A hashmap with multiple entries associated with the same key
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can use a List or Array to store multiple values under the same key in a HashMap.
---

**Contents**

[TOC]

#Solution

##Option 1: Using a List

A HashMap can store multiple values under the same key by using a List as the value. The following example illustrates how this can be done:

```java
HashMap<String, List<String>> map = new HashMap<>();
List<String> values = new ArrayList<>();
values.add("value1");
values.add("value2");
values.add("value3");
map.put("key", values);
```

##Option 2: Using an Array

A HashMap can also store multiple values under the same key by using an array as the value. The following example illustrates how this can be done:

```java
HashMap<String, String[]> map = new HashMap<>();
String[] values = new String[]{"value1", "value2", "value3"};
map.put("key", values);
```

##Option 3: Using a Set

A HashMap can also store multiple values under the same key by using a Set as the value. The following example illustrates how this can be done:

```java
HashMap<String, Set<String>> map = new HashMap<>();
Set<String> values = new HashSet<>();
values.add("value1");
values.add("value2");
values.add("value3");
map.put("key", values);
```

##Option 4: Using a Map

A HashMap can also store multiple values under the same key by using a Map as the value. The following example illustrates how this can be done:

```java
HashMap<String, Map<String, String>> map = new HashMap<>();
Map<String, String> values = new HashMap<>();
values.put("key1", "value1");
values.put("key2", "value2");
values.put("key3", "value3");
map.put("key", values);
```
