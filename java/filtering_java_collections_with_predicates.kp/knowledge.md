---
title: What is the process of filtering a Java collection using a predicate?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Filter a Java Collection by using the Collection.removeIf() method, passing in a Predicate to specify the conditions of the elements to be removed.
---

**Contents**

[TOC]

### Create Predicate
A predicate is a function that takes an object and returns a boolean value. In order to filter a Java Collection based on a predicate, the first step is to create a predicate that will test the object against the desired criteria. 

For example, if we wanted to filter a Collection of Strings to only include Strings that start with the letter 'A', we would create a predicate that tests each String to see if it starts with 'A':

```java
Predicate<String> startsWithA = s -> s.startsWith("A");
```

### Filter Collection
Once the predicate has been created, the Collection can be filtered using the `filter` method available on the Stream interface. This method takes the predicate as an argument and returns a Stream of elements that match the predicate.

For example, if we have a Collection of Strings and we want to filter it based on the predicate we created in the previous step, we can use the following code:

```java
List<String> strings = Arrays.asList("Apple", "Banana", "Carrot", "Avocado");

List<String> filteredStrings = strings.stream()
                                     .filter(startsWithA)
                                     .collect(Collectors.toList());
```

### Collect Filtered Elements
The filtered Stream can then be collected into a Collection using the `collect` method available on the Stream interface. This method takes a `Collector` as an argument, which is used to specify how the elements of the Stream should be collected.

For example, if we want to collect the filtered Strings into a List, we can use the `Collectors.toList()` method:

```java
List<String> filteredStrings = strings.stream()
                                     .filter(startsWithA)
                                     .collect(Collectors.toList());
```

### Use Filtered Collection
The filtered Collection can then be used as needed. In the example above, the filtered List will only contain Strings that start with the letter 'A':

```java
System.out.println(filteredStrings); // prints [Apple, Avocado]
```
