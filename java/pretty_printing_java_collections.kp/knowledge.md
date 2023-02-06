---
title: Creating an attractive output for Java collections using something other than tostring()
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use the toString() method in combination with the StringJoiner class to create a nicely formatted output.
---

**Contents**

[TOC]

### Using the toString() Method
The `toString()` method is the easiest way to print a Java collection. It returns a string representation of the collection, which is usually not very pretty. To make the output more readable, we can use the `String.format()` method to format the string before printing it:

```java
// Create a collection
List<String> list = Arrays.asList("Apple", "Banana", "Cherry");

// Print the collection using toString()
System.out.println(list.toString());

// Format the string before printing
System.out.println(String.format("%s, %s, and %s", list.get(0), list.get(1), list.get(2)));
```

### Using the Stream API
The Java Stream API makes it easy to print a collection in a more readable format. We can use the `forEach()` method to iterate over the elements of the collection and print them one by one:

```java
// Create a collection
List<String> list = Arrays.asList("Apple", "Banana", "Cherry");

// Print the collection using the Stream API
list.stream().forEach(System.out::println);
```

### Using the Iterator Interface
We can also use the `Iterator` interface to iterate over the elements of the collection and print them one by one:

```java
// Create a collection
List<String> list = Arrays.asList("Apple", "Banana", "Cherry");

// Create an iterator
Iterator<String> iterator = list.iterator();

// Iterate over the collection and print each element
while (iterator.hasNext()) {
    System.out.println(iterator.next());
}
```

### Using the for-each Loop
Finally, we can use the for-each loop to iterate over the elements of the collection and print them one by one:

```java
// Create a collection
List<String> list = Arrays.asList("Apple", "Banana", "Cherry");

// Iterate over the collection and print each element
for (String s : list) {
    System.out.println(s);
}
```
