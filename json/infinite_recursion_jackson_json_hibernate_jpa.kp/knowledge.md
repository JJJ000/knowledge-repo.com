---
title: Issue with Jackson json, hibernate jpa, and infinite recursion
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: To avoid infinite recursion with Jackson JSON and Hibernate JPA, use @JsonIgnore on the fields that cause the recursion.
---

**Contents**

[TOC]

**Section 1: Overview**

Infinite recursion is a common issue when using Jackson JSON and Hibernate JPA. It occurs when Jackson attempts to serialize an object that has a relationship to itself, resulting in an infinite loop of serialization. This can lead to performance issues, as Jackson will continue to serialize the same object over and over.

**Section 2: Causes**

The cause of this issue is that Jackson does not recognize the relationship between two objects. When Jackson encounters an object with a relationship to itself, it will attempt to serialize the object again, resulting in an infinite loop.

**Section 3: Solutions**

The solution to this issue is to use the @JsonIgnore annotation. This annotation tells Jackson to ignore the relationship between two objects, thus preventing the infinite loop.

**Section 4: Conclusion**

Infinite recursion is a common issue when using Jackson JSON and Hibernate JPA. The cause of this issue is that Jackson does not recognize the relationship between two objects. The solution to this issue is to use the @JsonIgnore annotation, which tells Jackson to ignore the relationship between two objects, thus preventing the infinite loop.
