---
title: Convert a Java 8 list of type v into a map of type k and v
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the Collectors.toMap() method to convert a List<V> into a Map<K, V>.
---

**Contents**

[TOC]

### Using Streams

We can use the `Collectors.toMap` method to convert a `List<V>` into a `Map<K, V>`. This method takes two arguments: a `Function` that specifies how to get the key from the `V` elements, and a `Function` that specifies how to get the values from the `V` elements.

For example, if we have a `List<Person>` and we want to convert it into a `Map<String, Person>` with the `Person`'s `name` as the key, we can do the following:

```java
Map<String, Person> personMap = list.stream()
    .collect(Collectors.toMap(Person::getName, Function.identity()));
```

### Using a For Loop

We can also use a `for` loop to iterate through the `List<V>` and add each element to the `Map<K, V>`.

For example, if we have a `List<Person>` and we want to convert it into a `Map<String, Person>` with the `Person`'s `name` as the key, we can do the following:

```java
Map<String, Person> personMap = new HashMap<>();
for (Person person : list) {
    personMap.put(person.getName(), person);
}
```

### Using Java 8 Lambdas

We can also use Java 8 Lambdas to convert a `List<V>` into a `Map<K, V>`.

For example, if we have a `List<Person>` and we want to convert it into a `Map<String, Person>` with the `Person`'s `name` as the key, we can do the following:

```java
Map<String, Person> personMap = list.stream()
    .collect(Collectors.toMap(Person::getName, Function.identity()));
```

### Using Guava

We can also use the `Maps.uniqueIndex` method from the [Guava](https://github.com/google/guava) library to convert a `List<V>` into a `Map<K, V>`. This method takes two arguments: a `Function` that specifies how to get the key from the `V` elements, and a `List<V>` of elements to be converted.

For example, if we have a `List<Person>` and we want to convert it into a `Map<String, Person>` with the `Person`'s `name` as the key, we can do the following:

```java
Map<String, Person> personMap = Maps.uniqueIndex(list, Person::getName);
```
