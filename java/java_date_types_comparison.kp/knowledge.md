---
title: Comparing java.util.date and java.sql.date
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: java.util.Date is a representation of a date and time, while java.sql.Date is a representation of only a date.
---

**Contents**

[TOC]

### Difference

The main difference between java.util.Date and java.sql.Date is that java.util.Date includes both date and time information, while java.sql.Date only includes the date information.

### Usage

java.util.Date is mainly used when interacting with classes in the java.text package, such as SimpleDateFormat. It is also used when interacting with Date-related classes in the java.time package, such as LocalDate and LocalDateTime.

java.sql.Date is mainly used when interacting with databases, such as SQLite and MySQL. It is also used when interacting with JDBC classes, such as PreparedStatement and ResultSet.

### Conversion

It is possible to convert between java.util.Date and java.sql.Date by using the toSqlDate() and toUtilDate() methods of the java.sql.Date class.
