---
title: What is the process for setting up a static map?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can initialise a static Map in Java by using the static block syntax to assign a new Map instance to the static Map variable.
---

**Contents**

[TOC]

`**` Create Map Instance**

The first step to initialise a static Map in Java is to create an instance of the Map. This can be done using the `new` keyword:

```
Map<String, Integer> myMap = new HashMap<>();
```

`**` Adding Elements to Map**

Once the Map instance has been created, elements can be added to the Map using the `put` method:

```
myMap.put("key1", 1);
myMap.put("key2", 2);
```

`**` Making Map Static**

To make the Map static, it must be declared as a static field in a class:

```
public class MyClass {
    public static Map<String, Integer> myMap = new HashMap<>();
}
```

`**` Accessing Map**

Once the Map is declared as a static field, it can be accessed from anywhere in the application using the class name:

```
int value = MyClass.myMap.get("key1");
```
