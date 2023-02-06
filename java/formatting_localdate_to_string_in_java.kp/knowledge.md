---
title: What is the best way to convert a localdate to a string?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use the DateTimeFormatter class to format a LocalDate to a String.
---

**Contents**

[TOC]

# Section 1: Import Necessary Classes

In order to format a LocalDate to a string, the `java.time.format.DateTimeFormatter` class needs to be imported.

```java
import java.time.LocalDate;
import java.time.format.DateTimeFormatter;
```

# Section 2: Create Formatter

Create a `DateTimeFormatter` object with the desired format. For example, if the desired format is yyyy-MM-dd, the following code can be used.

```java
DateTimeFormatter formatter = DateTimeFormatter.ofPattern("yyyy-MM-dd");
```

# Section 3: Create LocalDate

Create a `LocalDate` object with the desired date. For example, if the desired date is 2020-03-01, the following code can be used.

```java
LocalDate date = LocalDate.of(2020, 3, 1);
```

# Section 4: Format to String

Finally, format the `LocalDate` object to a string using the `format()` method.

```java
String formattedDate = date.format(formatter);
```

The `formattedDate` variable now contains the string "2020-03-01".
