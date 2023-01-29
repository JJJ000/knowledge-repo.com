---
title: Retrieve a single element from a Java stream
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the findFirst() method to get the first element from the Stream.
---

**Contents**

[TOC]

`**` Identifying the Element**

The first step in filtering a Java Stream to one and only one element is to identify which element should be the one chosen. This can be done by using a filtering method such as `filter()` or `findFirst()`. The filtering method should be passed a predicate that will identify the desired element. 

`**` Executing the Filter**

Once the desired element has been identified, the filter can be executed. This can be done by calling the `stream()` method on the data source and passing the filtering method to it. This will create a Stream object that contains only the desired element. 

`**` Retrieving the Element**

The next step is to retrieve the element from the Stream. This can be done by calling the `findFirst()` method on the Stream object. This will return an Optional object that contains the desired element. 

`**` Extracting the Element**

The final step is to extract the element from the Optional object. This can be done by calling the `get()` method on the Optional object. This will return the desired element, which is now the one and only element in the Stream.
