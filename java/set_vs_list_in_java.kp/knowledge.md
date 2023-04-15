---
title: How do set and list differ?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: A Set is an unordered collection of elements that cannot contain duplicates, while a List is an ordered collection of elements that can contain duplicates.
---

**Contents**

[TOC]

### Collection Type
Set is an interface that extends the Collection interface. List is an interface that extends the Collection interface and the Iterable interface. 

### Data Structure
Set is an unordered collection of objects in which duplicate values cannot be stored. List is an ordered collection of objects in which duplicate values can be stored. 

### Access
Set does not provide methods to access or modify elements by their index. List provides methods to access and modify elements by their index. 

### Performance
Set typically has better performance than List when it comes to searching and adding elements. List typically has better performance than Set when it comes to accessing and modifying elements.
