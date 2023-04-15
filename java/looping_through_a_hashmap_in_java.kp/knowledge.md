---
title: How to loop over the entries in a HashMap?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use an Iterator to iterate through the HashMap's entrySet.
---

**Contents**

[TOC]

### Iterating Through the HashMap

The most common way to iterate through a HashMap in Java is to use the entrySet() method. This method returns a Set view of the mappings contained in the HashMap. To iterate through the HashMap, you can use the enhanced for loop. Here is an example of how to do this:

```java
HashMap<String, Integer> map = new HashMap<>();
 
// add key-value pairs to the map
map.put("A", 1);
map.put("B", 2);
map.put("C", 3);
 
// iterate through the map
for (Map.Entry<String, Integer> entry : map.entrySet()) {
    System.out.println("Key = " + entry.getKey() + 
                       ", Value = " + entry.getValue());
}
```

### Iterating Through the Keys

Another way to iterate through a HashMap is to use the keySet() method. This method returns a Set view of the keys contained in the HashMap. To iterate through the keys, you can use the enhanced for loop. Here is an example of how to do this:

```java
HashMap<String, Integer> map = new HashMap<>();
 
// add key-value pairs to the map
map.put("A", 1);
map.put("B", 2);
map.put("C", 3);
 
// iterate through the keys
for (String key : map.keySet()) {
    System.out.println("Key = " + key);
}
```

### Iterating Through the Values

Another way to iterate through a HashMap is to use the values() method. This method returns a Collection view of the values contained in the HashMap. To iterate through the values, you can use the enhanced for loop. Here is an example of how to do this:

```java
HashMap<String, Integer> map = new HashMap<>();
 
// add key-value pairs to the map
map.put("A", 1);
map.put("B", 2);
map.put("C", 3);
 
// iterate through the values
for (Integer value : map.values()) {
    System.out.println("Value = " + value);
}
```

### Iterating Through the Entries

Finally, you can also iterate through the entries of a HashMap using the entrySet() method. This method returns a Set view of the mappings contained in the HashMap. To iterate through the entries, you can use the enhanced for loop. Here is an example of how to do this:

```java
HashMap<String, Integer> map = new HashMap<>();
 
// add key-value pairs to the map
map.put("A", 1);
map.put("B", 2);
map.put("C", 3);
 
// iterate through the entries
for (Map.Entry<String, Integer> entry : map.entrySet()) {
    System.out.println("Key = " + entry.getKey() + 
                       ", Value = " + entry.getValue());
}
```
