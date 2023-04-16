---
title: What is the method for finding the common elements of two sets?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To calculate the intersection of two sets in Java, use the retainAll() method on one set, passing in the other set as an argument.
---

**Contents**

[TOC]

# Section 1: Understanding the Concept of Intersection

Intersection is a mathematical concept that describes the common elements between two sets. It is represented by the symbol ∩ and is defined as the set of all elements that are common to both sets. For example, if set A contains elements {1, 2, 3, 4} and set B contains elements {2, 3, 4, 5}, then the intersection of A and B is {2, 3, 4}.

# Section 2: Implementing Intersection in Java

In Java, the intersection of two sets can be calculated using the retainAll() method. This method takes in a set as an argument and removes all elements from the set that are not present in the argument set. The resulting set will be the intersection of the two sets. 

For example, the following code calculates the intersection of two sets A and B:

```
Set<Integer> A = new HashSet<>(Arrays.asList(1, 2, 3, 4));
Set<Integer> B = new HashSet<>(Arrays.asList(2, 3, 4, 5));

A.retainAll(B);

System.out.println(A); // prints {2, 3, 4}
```

# Section 3: Using Streams to Calculate Intersection

In Java 8 and above, the intersection of two sets can also be calculated using streams. The stream() method can be used to convert the set into a stream, and the filter() method can be used to filter the elements that are present in both sets. The resulting stream can then be collected into a set using the collect() method. 

For example, the following code calculates the intersection of two sets A and B using streams:

```
Set<Integer> A = new HashSet<>(Arrays.asList(1, 2, 3, 4));
Set<Integer> B = new HashSet<>(Arrays.asList(2, 3, 4, 5));

Set<Integer> intersection = A.stream()
    .filter(B::contains)
    .collect(Collectors.toSet());

System.out.println(intersection); // prints {2, 3, 4}
```

# Section 4: Optimizing Performance

It is important to note that the performance of the retainAll() method and the stream() method can vary depending on the size of the sets. For large sets, the retainAll() method may be more efficient as it only requires one iteration over the set. For smaller sets, the stream() method may be more efficient as it can take advantage of parallelism. 

It is also important to note that the retainAll() method modifies the original set, while the stream() method does not. Therefore, if the original sets need to be preserved, the stream() method should be used.
