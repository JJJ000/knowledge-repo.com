---
title: What is the purpose of the string.chars() method in Java 8, and why does it produce a stream of integers?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: String.chars() is a stream of ints in Java 8 because it returns a stream of ints representing the characters in the String.
---

**Contents**

[TOC]

# Overview
String.chars() is a method introduced in Java 8 which returns a stream of ints representing the characters of the String. This method is useful for processing the characters of a String in a functional style.

# Reason 1: Streams are Intuitive
Streams are a powerful tool for processing data in Java 8, and they are intuitive to use. By returning a stream of ints, String.chars() allows developers to easily process the characters of a String in a functional style.

# Reason 2: Efficient Processing
Using a stream of ints is much more efficient than using a stream of characters. This is because ints take up less memory than characters, and the ints can be processed faster than characters.

# Reason 3: Simple to Use
Using a stream of ints is also simpler than using a stream of characters. This is because it is easier to process a stream of ints than a stream of characters. Additionally, the ints can be used to easily index into an array of characters.
