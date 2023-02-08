---
title: What is the process for looping through a jsonobject?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: Use a for-each loop to iterate over the JSONObject`s keys and access the corresponding values.
---

**Contents**

[TOC]

#1 Iterating with a for loop

The most common way to iterate over a JSONObject is to use a for loop. This loop will iterate over all the key-value pairs in the JSONObject.

```
for (String key : jsonObject.keys()) { 
  Object value = jsonObject.get(key);
  // do something with the key and value
}
```

#2 Iterating with an Iterator

Another way to iterate over a JSONObject is to use an Iterator. This approach is useful if you need to access the keys and values in a specific order.

```
Iterator<String> keys = jsonObject.keys();
while (keys.hasNext()) {
  String key = keys.next();
  Object value = jsonObject.get(key);
  // do something with the key and value
}
```

#3 Iterating with a for-each loop

Another way to iterate over a JSONObject is to use a for-each loop. This approach is useful if you need to access the keys and values in a specific order.

```
for (Map.Entry<String, Object> entry : jsonObject.entrySet()) {
  String key = entry.getKey();
  Object value = entry.getValue();
  // do something with the key and value
}
```

#4 Iterating with a Stream

The last way to iterate over a JSONObject is to use a Stream. This approach is useful if you need to perform some operation on each key-value pair.

```
jsonObject.entrySet().stream()
  .forEach(entry -> {
    String key = entry.getKey();
    Object value = entry.getValue();
    // do something with the key and value
  });
```
