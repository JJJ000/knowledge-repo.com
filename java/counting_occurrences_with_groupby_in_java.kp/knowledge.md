---
title: What is the best way to count the number of occurrences with groupby?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can count occurrences with groupBy in Java by using the Collectors.groupingBy() and Collectors.counting() methods.
---

**Contents**

[TOC]

1. **Create a Map of Occurrences:**

Using the Java Stream API, you can group elements of a list by a certain criteria and then count the occurrences of each group. To do this, you can use the `Collectors.groupingBy()` method to create a `Map` of occurrences. The `groupingBy()` method takes two parameters: a `Function` to define the criteria used to group the elements, and a `Collector` to define how the elements in each group are collected.

2. **Count the Occurrences:**

To count the occurrences of each group, you can use the `Collectors.counting()` method. The `counting()` method takes no parameters and returns a `Collector` that counts the number of elements in each group.

3. **Print the Results:**

Once you have the Map of occurrences, you can print the results with a `forEach()` loop. This loop will iterate over each entry in the Map and print the group and the number of occurrences.

4. **Example:**

For example, let's say we have a list of `Person` objects with a `String` field called `name`, and we want to count the number of occurrences of each name in the list. We can use the `groupingBy()` and `counting()` methods to achieve this:

```java
Map<String, Long> nameCounts = 
    people.stream()
          .collect(Collectors.groupingBy(Person::getName, Collectors.counting()));

nameCounts.forEach((name, count) -> System.out.println(name + ": " + count));
```

The `nameCounts` Map will contain the name of each person in the list, and the number of occurrences of that name. The `forEach()` loop will then print each name and its corresponding count.
