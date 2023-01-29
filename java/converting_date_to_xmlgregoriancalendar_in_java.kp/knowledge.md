---
title: Convert java.util.date to xmlgregoriancalendar
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the `toGregorianCalendar()` method to convert a java.util.Date to an XMLGregorianCalendar.
---

**Contents**

[TOC]

### Conversion

The following code snippet can be used to convert a java.util.Date object to an XMLGregorianCalendar object:

```java
Date date = new Date();
XMLGregorianCalendar xmlGregorianCalendar = DatatypeFactory.newInstance().newXMLGregorianCalendar(new GregorianCalendar(TimeZone.getTimeZone("UTC")));
xmlGregorianCalendar.setTime(date.getTime(), DatatypeConstants.FIELD_UNDEFINED);
```

### Explanation

The code snippet first creates a java.util.Date object. Then, it creates an XMLGregorianCalendar object using the DatatypeFactory. The GregorianCalendar object is created using the UTC timezone, so that the timezone of the XMLGregorianCalendar object is set to UTC. Finally, the time of the XMLGregorianCalendar object is set to the time of the java.util.Date object, with the second parameter of the setTime() method set to DatatypeConstants.FIELD_UNDEFINED, which means that the milliseconds will be set to an unspecified value.

### Advantages

Using this method of conversion has the advantage of ensuring that the timezone of the XMLGregorianCalendar object is set to UTC, which will ensure that the time is consistent across different timezones.

### Disadvantages

The main disadvantage of this method is that it is not very efficient, as it requires the creation of multiple objects.
