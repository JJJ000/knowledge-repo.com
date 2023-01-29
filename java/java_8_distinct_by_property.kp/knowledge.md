---
title: Distinct elements in Java 8 by property
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The Stream API`s distinct() method can be used to filter a stream to only include distinct objects based on a specific property.
---

**Contents**

[TOC]

`**` Using Streams**

We can use Java 8 Streams to distinct elements by property. To do this, we need to use the distinct() method on a Stream, which will return a Stream with distinct elements based on the property passed as a parameter.

For example, if we have a list of Person objects, we can use the distinct() method to get a Stream of Person objects with distinct names:

```
List<Person> people = ...
Stream<Person> distinctPeople = people.stream().distinct(Comparator.comparing(Person::getName));
```

`**` Using Collectors**

We can also use Java 8 Collectors to distinct elements by property. To do this, we need to use the toMap() collector, which will return a Map of distinct elements based on the property passed as a parameter.

For example, if we have a list of Person objects, we can use the toMap() collector to get a Map of Person objects with distinct names:

```
List<Person> people = ...
Map<String, Person> distinctPeople = people.stream().collect(Collectors.toMap(Person::getName, Function.identity(), (p1, p2) -> p1));
```

`**` Using GroupingBy**

We can also use Java 8 GroupingBy to distinct elements by property. To do this, we need to use the groupingBy() collector, which will return a Map of distinct elements based on the property passed as a parameter.

For example, if we have a list of Person objects, we can use the groupingBy() collector to get a Map of Person objects with distinct names:

```
List<Person> people = ...
Map<String, List<Person>> distinctPeople = people.stream().collect(Collectors.groupingBy(Person::getName));
```

`**` Using Set**

Finally, we can use Java 8 Set to distinct elements by property. To do this, we need to use the addAll() method on a Set, which will return a Set of distinct elements based on the property passed as a parameter.

For example, if we have a list of Person objects, we can use the addAll() method to get a Set of Person objects with distinct names:

```
List<Person> people = ...
Set<Person> distinctPeople = new HashSet<>();
distinctPeople.addAll(people.stream().collect(Collectors.toSet(Person::getName)));
```
