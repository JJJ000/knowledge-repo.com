---
title: What is the process for changing an existing value in a hashmap, using a given key?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the put() method on the HashMap, passing in the key and the new value.
---

**Contents**

[TOC]

####1. Retrieve the HashMap

In order to update a value, given a key in a HashMap, the HashMap must first be retrieved. This can be done by creating a reference to the HashMap and assigning it the HashMap object. 

```
HashMap<String, String> myHashMap = new HashMap<String, String>();
```

####2. Add or Update the Value

Once the HashMap is retrieved, the value can be updated by using the `put()` method. This method takes two arguments, the key and the value, and adds the key-value pair to the HashMap. If the key already exists in the HashMap, the value will be updated to the new value. 

```
myHashMap.put("key", "newValue");
```

####3. Verify the Update

Finally, the updated value can be verified by using the `get()` method. This method takes one argument, the key, and returns the associated value. 

```
String updatedValue = myHashMap.get("key");
```

####4. Iterate Through the HashMap

If desired, the HashMap can be iterated through to view all of the key-value pairs. This can be done by using the `entrySet()` method. 

```
for (Map.Entry<String, String> entry : myHashMap.entrySet()) {
    System.out.println("Key: " + entry.getKey() + " Value: " + entry.getValue());
}
```
