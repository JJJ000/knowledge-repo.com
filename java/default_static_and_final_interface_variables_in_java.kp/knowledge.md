---
title: What is the reasoning behind making interface variables static and final by default?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Interface variables are static and final by default in Java to ensure that all implementations of the interface use the same value for the variable.
---

**Contents**

[TOC]

### Static
Interface variables are static because they are associated with the interface, not with any object created from the interface. This means that static interface variables are shared by all objects that implement the interface.

### Final
Interface variables are final by default because they are constants that must not be changed. Allowing them to be changed would create potential conflicts between objects that use the same interface.
