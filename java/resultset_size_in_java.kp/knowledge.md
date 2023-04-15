---
title: What is the size of a java.sql.resultset?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The size of a java.sql.ResultSet can be obtained by calling the ResultSet.getRow() method.
---

**Contents**

[TOC]

1. Overview
------------------
The size of a java.sql.ResultSet can be determined by using the method ResultSet.getRow() which returns the current row number, or by using the method ResultSet.last() which moves the cursor to the last row and returns the row number. 

2. Using ResultSet.getRow()
------------------
The ResultSet.getRow() method returns the current row number in the ResultSet. This method should be used when the ResultSet is not empty and the cursor is at the beginning of the ResultSet. 

```java
// Get the size of the ResultSet
int size = 0;

if (resultSet.isBeforeFirst()) {
    resultSet.next();
    size = resultSet.getRow();
}
```

3. Using ResultSet.last()
------------------
The ResultSet.last() method moves the cursor to the last row in the ResultSet and returns the row number. This method should be used when the ResultSet is not empty and the cursor is not at the beginning of the ResultSet.

```java
// Get the size of the ResultSet
int size = 0;

if (resultSet.last()) {
    size = resultSet.getRow();
}
```

4. Conclusion
------------------
The size of a java.sql.ResultSet can be determined by using the ResultSet.getRow() or ResultSet.last() methods. Both of these methods should be used depending on the position of the cursor in the ResultSet.
