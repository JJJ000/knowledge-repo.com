---
title: Convert the format of a Java string to a different date format
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the SimpleDateFormat class to format the date string into the desired format.
---

**Contents**

[TOC]

### Using SimpleDateFormat
SimpleDateFormat is a concrete class for formatting and parsing dates in a locale-sensitive manner. It allows for formatting (date → text), parsing (text → date), and normalization.

To change a date format in a Java string, you can use the SimpleDateFormat class. You can create a SimpleDateFormat instance and specify the desired date and time pattern. Then you can use the format() method to format the date into a string.

For example, if you have a string that contains a date in the format "yyyy/MM/dd", you can use the following code to change the date format to "MM/dd/yyyy":

```
String dateString = "2020/05/30";
SimpleDateFormat formatter = new SimpleDateFormat("MM/dd/yyyy");
String output = formatter.format(dateString);
```

### Using String.replace()
The String.replace() method can be used to change the format of a date string. This method takes two parameters: the substring to be replaced and the substring to be used as a replacement.

For example, if you have a string that contains a date in the format "yyyy/MM/dd", you can use the following code to change the date format to "MM/dd/yyyy":

```
String dateString = "2020/05/30";
String output = dateString.replace("yyyy/MM/dd", "MM/dd/yyyy");
```

### Using DateTimeFormatter
The DateTimeFormatter class is a formatter that can be used to parse and format dates and times. It is part of the Java 8 Date/Time API. To change a date format in a Java string, you can use the DateTimeFormatter class.

For example, if you have a string that contains a date in the format "yyyy/MM/dd", you can use the following code to change the date format to "MM/dd/yyyy":

```
String dateString = "2020/05/30";
DateTimeFormatter formatter = DateTimeFormatter.ofPattern("MM/dd/yyyy");
String output = formatter.format(dateString);
```

### Using LocalDate
The LocalDate class is part of the Java 8 Date/Time API. It represents a date without time-zone information. To change a date format in a Java string, you can use the LocalDate class.

For example, if you have a string that contains a date in the format "yyyy/MM/dd", you can use the following code to change the date format to "MM/dd/yyyy":

```
String dateString = "2020/05/30";
LocalDate date = LocalDate.parse(dateString, DateTimeFormatter.ofPattern("yyyy/MM/dd"));
String output = date.format(DateTimeFormatter.ofPattern("MM/dd/yyyy"));
```
