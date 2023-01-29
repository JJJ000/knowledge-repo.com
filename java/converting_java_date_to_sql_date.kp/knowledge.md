---
title: What is the process for transforming a java.util.date to a java.sql.date?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the java.sql.Date constructor with a java.util.Date parameter to convert a java.util.Date to a java.sql.Date.
---

**Contents**

[TOC]

### Overview

The java.util.Date class is used to represent a date and time, while the java.sql.Date class is used to represent a date in the database. Converting between the two classes is a simple process.

### Convert java.util.Date to java.sql.Date

The java.sql.Date class has a constructor that takes a java.util.Date object as an argument. To convert a java.util.Date object to a java.sql.Date object, simply pass the java.util.Date object to the java.sql.Date constructor.

### Example

The following example shows how to convert a java.util.Date object to a java.sql.Date object:

```java
// Create a java.util.Date object
java.util.Date utilDate = new java.util.Date();

// Convert to java.sql.Date
java.sql.Date sqlDate = new java.sql.Date(utilDate.getTime());
```

### Conclusion

In conclusion, converting a java.util.Date object to a java.sql.Date object is a simple process. All you need to do is pass the java.util.Date object to the java.sql.Date constructor.
