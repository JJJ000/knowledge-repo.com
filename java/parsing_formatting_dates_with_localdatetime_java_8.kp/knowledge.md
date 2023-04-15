---
title: What is the best way to work with localdatetime to parse and format dates in Java 8?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: You can parse/format dates with LocalDateTime using the LocalDateTime.parse() and LocalDateTime.format() methods.
---

**Contents**

[TOC]

`**` Creating a LocalDateTime Object**

LocalDateTime is a class in the Java 8 Date-Time API that represents a date-time without a time-zone. To create a LocalDateTime object, you can use the `LocalDateTime.of(int year, int month, int dayOfMonth, int hour, int minute)` static method. This method takes five parameters representing the year, month, day of the month, hour, and minute, respectively. 

For example, to create a LocalDateTime object representing the date-time `2020-10-01T10:15`, you can use the following code:

```java
LocalDateTime dateTime = LocalDateTime.of(2020, 10, 1, 10, 15);
```

`**` Parsing a String to a LocalDateTime Object**

You can also parse a string representing a date-time into a LocalDateTime object. To do this, you can use the `LocalDateTime.parse(String text)` static method. This method takes a single parameter representing the string to be parsed. The string must be in the format `yyyy-MM-ddTHH:mm`, where `yyyy` is the four-digit year, `MM` is the two-digit month, `dd` is the two-digit day, `HH` is the two-digit hour, and `mm` is the two-digit minute. 

For example, to parse the string `2020-10-01T10:15` into a LocalDateTime object, you can use the following code:

```java
LocalDateTime dateTime = LocalDateTime.parse("2020-10-01T10:15");
```

`**` Formatting a LocalDateTime Object to a String**

You can also format a LocalDateTime object to a string. To do this, you can use the `LocalDateTime.format(DateTimeFormatter formatter)` instance method. This method takes a single parameter representing the formatter to be used. The formatter must be an instance of the `DateTimeFormatter` class. 

For example, to format a LocalDateTime object to the format `dd-MM-yyyy HH:mm`, you can use the following code:

```java
String formattedDateTime = dateTime.format(DateTimeFormatter.ofPattern("dd-MM-yyyy HH:mm"));
```

`**` Other Useful Methods**

In addition to the methods mentioned above, there are several other useful methods in the LocalDateTime class. These include methods for adding or subtracting days, months, or years, methods for comparing two LocalDateTime objects, and methods for getting the current date-time. For more information, please see the [LocalDateTime Javadocs](https://docs.oracle.com/javase/8/docs/api/java/time/LocalDateTime.html).
