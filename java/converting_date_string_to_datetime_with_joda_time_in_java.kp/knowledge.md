---
title: Using the joda time library, transforming a date string into a datetime object
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The Joda Time library can be used to convert a date string to a DateTime object in Java by calling the DateTime.parse() method.
---

**Contents**

[TOC]

##### 1. Import Joda Time Library 
To use Joda Time library in Java, you need to import the library in your code.

```java
import org.joda.time.DateTime;
```

##### 2. Create DateTimeFormatter

Next, you need to create a DateTimeFormatter object to parse the date string.

```java
DateTimeFormatter formatter = DateTimeFormat.forPattern("dd/MM/yyyy");
```

##### 3. Parse Date String

Finally, you can use the parseDateTime method to parse the date string and create a DateTime object.

```java 
DateTime dateTime = formatter.parseDateTime("13/04/2020");
```

##### 4. Print DateTime Object

To verify that the DateTime object was created successfully, you can print it out.

```java
System.out.println(dateTime);
```

The output should be: `2020-04-13T00:00:00.000Z`
