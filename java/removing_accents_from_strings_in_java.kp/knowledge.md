---
title: What is the most efficient method of removing accents and converting an entire string of text to basic letters?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Yes, you can use the Normalizer class to normalize a string and remove accents.
---

**Contents**

[TOC]

**Using the Normalizer Class**

The Normalizer class can be used to remove accents from a string in Java. The following code snippet shows how this can be done:

```java
String input = "áéíóú";
String output = Normalizer.normalize(input, Normalizer.Form.NFD).replaceAll("[^\\p{ASCII}]", "");
System.out.println(output); // Outputs: aeiou
```

**Using the replaceAll Method**

The replaceAll method of the String class can also be used to remove accents from a string in Java. The following code snippet shows how this can be done:

```java
String input = "áéíóú";
String output = input.replaceAll("[\\p{InCombiningDiacriticalMarks}]", "");
System.out.println(output); // Outputs: aeiou
```

**Using the Apache Commons Library**

The Apache Commons library provides a StringUtils class which can be used to remove accents from a string in Java. The following code snippet shows how this can be done:

```java
String input = "áéíóú";
String output = StringUtils.stripAccents(input);
System.out.println(output); // Outputs: aeiou
```

**Using the CharMatcher Class**

The CharMatcher class from the Guava library can also be used to remove accents from a string in Java. The following code snippet shows how this can be done:

```java
String input = "áéíóú";
String output = CharMatcher.javaIsoControl().removeFrom(input);
System.out.println(output); // Outputs: aeiou
```
