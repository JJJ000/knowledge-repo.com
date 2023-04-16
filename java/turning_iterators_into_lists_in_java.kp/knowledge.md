---
title: Turn an iterator into a list
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can convert an Iterator to a List in Java by using the List constructor and passing in the Iterator as an argument.
---

**Contents**

[TOC]

# Section 1: Overview

An Iterator is an object that enables a programmer to traverse through a Collection, such as a List or Set. It provides a way to access elements of a Collection one at a time, without having to know the internal structure of the Collection. The Iterator in Java is an interface that is part of the Java Collection Framework.

# Section 2: How to Convert

In order to convert an Iterator to a List in Java, the Iterator must first be converted to an Iterable. This can be done by using the Iterator's built-in forEachRemaining() method. Once the Iterator is an Iterable, it can then be used to create a List using the Java Stream API. The Stream API provides a convenient way to convert an Iterable to a List using the collect() method.

# Section 3: Example

In the following example, an Iterator is used to traverse a List of Strings. The Iterator is first converted to an Iterable using the forEachRemaining() method. The Iterable is then used to create a List using the collect() method of the Stream API.

```
List<String> list = Arrays.asList("foo", "bar", "baz");
Iterator<String> iterator = list.iterator();
Iterable<String> iterable = () -> iterator;
List<String> newList = StreamSupport.stream(iterable.spliterator(), false)
                                   .collect(Collectors.toList());
```

# Section 4: Conclusion

Converting an Iterator to a List in Java is a simple process. By first converting the Iterator to an Iterable using the forEachRemaining() method, and then using the Stream API to create a List from the Iterable, the Iterator can be easily converted to a List.
