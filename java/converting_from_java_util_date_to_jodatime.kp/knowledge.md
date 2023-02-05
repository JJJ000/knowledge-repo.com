---
title: Change a java.util.date to a jodatime object
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the DateTime constructor to convert a java.util.Date to a JodaTime DateTime object.
---

**Contents**

[TOC]

### Step 1: Import JodaTime Library

In order to convert from `java.util.date` to `JodaTime`, first we need to import the JodaTime library.

```java
import org.joda.time.DateTime;
```

### Step 2: Create a DateTime Object

Once we have imported the JodaTime library, we can create a `DateTime` object from the `java.util.date` object.

```java
DateTime dateTime = new DateTime(java.util.date);
```

### Step 3: Format the DateTime Object

If needed, we can format the `DateTime` object to a specific format.

```java
String formattedDateTime = dateTime.toString("yyyy-MM-dd HH:mm:ss");
```

### Step 4: Print the Formatted DateTime

Finally, we can print the formatted `DateTime` to the console.

```java
System.out.println(formattedDateTime);
```
