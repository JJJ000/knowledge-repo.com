---
title: What is the best way to iterate through a jsonobject in Android to access each key and its associated value?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: You can loop through a flat JSON object by using the keys() method of the JSONObject, then using get() to get the value associated with each key.
---

**Contents**

[TOC]

**Section 1: Using a For Loop**

You can use a for loop to loop through a flat JSON object and get each key and value. The syntax for this is as follows:

```
for (String key : jsonObject.keySet()) {
    Object value = jsonObject.get(key);
    // Do something with key and value
}
```

The `keySet()` method returns a set of keys in the JSONObject, which can then be used to loop through the object. The `get()` method is used to get the value associated with the key.

**Section 2: Using an Iterator**

You can also use an iterator to loop through a flat JSON object and get each key and value. The syntax for this is as follows:

```
Iterator<String> iter = jsonObject.keys();
while (iter.hasNext()) {
    String key = iter.next();
    Object value = jsonObject.get(key);
    // Do something with key and value
}
```

The `keys()` method returns an iterator of keys in the JSONObject, which can then be used to loop through the object. The `get()` method is used to get the value associated with the key.

**Section 3: Using a forEach Loop**

You can also use a forEach loop to loop through a flat JSON object and get each key and value. The syntax for this is as follows:

```
jsonObject.forEach((key, value) -> {
    // Do something with key and value
});
```

The `forEach()` method takes a lambda expression, which is used to loop through the object. The key and value are passed as parameters to the lambda expression, which can then be used to do something with the key and value.

**Section 4: Using an Enhanced For Loop**

You can also use an enhanced for loop to loop through a flat JSON object and get each key and value. The syntax for this is as follows:

```
for (Map.Entry<String, Object> entry : jsonObject.entrySet()) {
    String key = entry.getKey();
    Object value = entry.getValue();
    // Do something with key and value
}
```

The `entrySet()` method returns a set of entries in the JSONObject, which can then be used to loop through the object. The `getKey()` and `getValue()` methods are used to get the key and value associated with the entry.
