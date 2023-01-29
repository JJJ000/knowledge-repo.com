---
title: What is the process for reversing the result of a method reference predicate?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: A method reference predicate can be negated by applying the logical negation operator (!) to the method reference.
---

**Contents**

[TOC]

### Understanding Method Reference Predicates

A method reference predicate is a type of predicate, which is a boolean-valued function of one argument. In Java, a method reference predicate is a method that can be used to test the truth of a given expression, such as when using the Stream API.

### Negating a Method Reference Predicate

The way to negate a method reference predicate is to use the `negate()` method in the `Predicate` interface. This method takes a predicate as an argument and returns a new predicate that is the logical negation of the original predicate.

### Example

For example, suppose we have a method reference predicate `isEven` that tests whether an integer is even. We can negate this predicate by using the `negate()` method as follows:

```
Predicate<Integer> isOdd = isEven.negate();
```

### Usage

The negated predicate can then be used in the same way as any other predicate. For example, it can be passed to the `filter()` method of a `Stream` object to filter out all odd numbers:

```
List<Integer> oddNumbers = myList.stream().filter(isOdd).collect(Collectors.toList());
```
