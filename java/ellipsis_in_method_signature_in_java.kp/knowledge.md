---
title: What does the ellipsis (...) represent in this method signature?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The ellipsis (...) in the method signature indicates that the method can accept a variable number of arguments.
---

**Contents**

[TOC]

**Purpose:**
The ellipsis (...) indicates that the method can be passed a variable number of arguments.

**Syntax:**
The ellipsis is used in the method signature to indicate that the method can take in a variable number of arguments. It is placed after the type of the arguments that the method can take.

**Example:**
For example, a method signature for a method that can take in a variable number of String arguments would look like this:

`public void printStrings(String... strings)`
