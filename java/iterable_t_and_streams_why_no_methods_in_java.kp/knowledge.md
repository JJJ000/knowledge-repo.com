---
title: What is the reason iterable<t> does not offer stream() and parallelstream() methods?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The Iterable interface does not provide stream() and parallelStream() methods because it is not a collection type.
---

**Contents**

[TOC]

# Reason 1: Iterable<T> is not a Collection
Iterable<T> is an interface in the Java Collection framework, but it is not a Collection. The Collection interface extends Iterable<T>, and it is the Collection interface that provides the stream() and parallelStream() methods.

# Reason 2: Streams are not a Core Concept of Iterable<T>
Streams are a relatively new concept in Java, and they are not a core concept of Iterable<T>. Streams are more focused on functional-style operations, which are not the focus of Iterable<T>.

# Reason 3: Streams are not Necessary for Iterable<T>
Iterable<T> provides basic iteration capabilities, and streams are not necessary for this purpose. Streams are more useful for complex operations, such as filtering, mapping, and reducing.

# Reason 4: Streams Are Not Efficient for Iterable<T>
Streams are designed to be more efficient than traditional iteration, but they are not always the best choice for iterating over an Iterable<T>. Streams can be more expensive than traditional iteration in certain cases, so it is more efficient to use traditional iteration when possible.
