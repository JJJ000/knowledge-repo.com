---
title: What is the process for looping through a jsonobject?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use a for loop to iterate over the JSONObject`s keys, and use the get() method to access the associated values.
---

**Contents**

[TOC]

### Setup

1. Create a JSONObject.

```java
JSONObject obj = new JSONObject();
```

2. Add key-value pairs to the JSONObject.

```java
obj.put("name", "John");
obj.put("age", 25);
```

### Iterate Using EntrySet

1. Use the entrySet() method to get the entry set of the JSONObject.

```java
Set<Map.Entry<String, Object>> entries = obj.entrySet();
```

2. Iterate over the entry set using an enhanced for loop.

```java
for (Map.Entry<String, Object> entry : entries) {
    String key = entry.getKey();
    Object value = entry.getValue();
    // Do something with the key and value
}
```

### Iterate Using Keys

1. Use the keySet() method to get the set of keys in the JSONObject.

```java
Set<String> keys = obj.keySet();
```

2. Iterate over the key set using an enhanced for loop.

```java
for (String key : keys) {
    Object value = obj.get(key);
    // Do something with the key and value
}
```

### Iterate Using Values

1. Use the values() method to get the collection of values in the JSONObject.

```java
Collection<Object> values = obj.values();
```

2. Iterate over the collection of values using an enhanced for loop.

```java
for (Object value : values) {
    // Do something with the value
}
```
