---
title: What is the return type of collections.emptylist()?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Yes, Collections.emptyList() returns an immutable List<Object> in Java.
---

**Contents**

[TOC]

## Overview
Collections.emptyList() is a static factory method of the java.util.Collections class. It returns an immutable List object with no elements. The returned List is of the Object type, meaning it can contain any type of object.

## Returned Type
The returned List is of the Object type. This means that it can contain any type of object. It is not a List of a specific type of object, such as a List of Strings or a List of Integers.

## Immutability
The List returned by Collections.emptyList() is immutable. This means that the list cannot be modified after it has been created. Any attempts to modify the list will result in an UnsupportedOperationException.

## Usage
Collections.emptyList() can be used when a List is needed, but no elements need to be added to the list. It is also useful when a List is needed, but the elements of the list are not known at the time of creation.
