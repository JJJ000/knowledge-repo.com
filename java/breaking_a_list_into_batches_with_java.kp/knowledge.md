---
title: What is a commonly used Java tool for dividing a list into sections?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: No, there is not a common Java utility to break a list into batches.
---

**Contents**

[TOC]

## Iterate Through List

The most basic way to break a list into batches is to iterate through the list, and split the elements into batches of a given size. This can be done with a simple for loop:

```
List<List<Object>> batches = new ArrayList<>();

for (int i = 0; i < list.size(); i += batchSize) {
    batches.add(list.subList(i, Math.min(i + batchSize, list.size())));
}
```

## Guava Splitter

The [Guava Splitter](https://guava.dev/releases/19.0/api/docs/com/google/common/base/Splitter.html) class can be used to break a list into batches. This uses the `fixedLength()` method, which returns a `List<String>` with each element being a batch of the given size:

```
List<String> batches = Splitter.fixedLength(batchSize).splitToList(list);
```

## Stream API

The Java Stream API can also be used to break a list into batches. This uses the `collect()` method, which collects the elements into a `List`:

```
List<List<Object>> batches = list.stream()
    .collect(Collectors.groupingBy(it -> it / batchSize))
    .values();
```

## Apache Commons Lang

The [Apache Commons Lang](https://commons.apache.org/proper/commons-lang/apidocs/org/apache/commons/lang3/ArrayUtils.html) library provides the `partition()` method, which can be used to break a list into batches:

```
List<Object[]> batches = ArrayUtils.partition(list.toArray(), batchSize);
```
