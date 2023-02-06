---
title: How can I divide an arraylist into multiple smaller arraylists using java?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can split an ArrayList into multiple small ArrayLists by using the subList() method.
---

**Contents**

[TOC]

### Section 1: Iterating Through the Original ArrayList
One way to split an ArrayList into multiple small ArrayLists is to iterate through the original ArrayList and add each element to a new ArrayList. The following code shows an example of this approach:

```java
ArrayList<String> originalList = new ArrayList<>(Arrays.asList("a", "b", "c", "d", "e"));

ArrayList<String> list1 = new ArrayList<>();
ArrayList<String> list2 = new ArrayList<>();

for (String element : originalList) {
  if (list1.size() < 3) {
    list1.add(element);
  } else {
    list2.add(element);
  }
}
```

### Section 2: Using the SubList Method
Another way to split an ArrayList into multiple small ArrayLists is to use the `subList()` method. This method returns a view of the portion of the original ArrayList between the specified `fromIndex` and `toIndex`. The following code shows an example of this approach:

```java
ArrayList<String> originalList = new ArrayList<>(Arrays.asList("a", "b", "c", "d", "e"));

ArrayList<String> list1 = new ArrayList<>(originalList.subList(0, 3));
ArrayList<String> list2 = new ArrayList<>(originalList.subList(3, 5));
```

### Section 3: Using the Split Method
A third way to split an ArrayList into multiple small ArrayLists is to use the `split()` method. This method takes an argument that specifies the maximum number of elements in each ArrayList. The following code shows an example of this approach:

```java
ArrayList<String> originalList = new ArrayList<>(Arrays.asList("a", "b", "c", "d", "e"));

List<ArrayList<String>> lists = originalList.split(3);
ArrayList<String> list1 = lists.get(0);
ArrayList<String> list2 = lists.get(1);
```

### Section 4: Using the Partition Method
A fourth way to split an ArrayList into multiple small ArrayLists is to use the `partition()` method. This method takes an argument that specifies the maximum number of elements in each ArrayList. The following code shows an example of this approach:

```java
ArrayList<String> originalList = new ArrayList<>(Arrays.asList("a", "b", "c", "d", "e"));

List<List<String>> lists = originalList.partition(3);
ArrayList<String> list1 = (ArrayList<String>) lists.get(0);
ArrayList<String> list2 = (ArrayList<String>) lists.get(1);
```
