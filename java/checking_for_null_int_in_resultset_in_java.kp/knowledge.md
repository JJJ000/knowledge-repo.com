---
title: Determining if an integer from a Java resultset is equal to zero
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Use the ResultSet`s wasNull() method to check if the value retrieved from the ResultSet is null.
---

**Contents**

[TOC]

**Checking for a Null Int Value**

1. **Using the ResultSet getInt() Method**

The ResultSet getInt() method can be used to retrieve an int value from a ResultSet. This method will return 0 if the value is null. Therefore, it is not possible to determine if a value is null using this method.

2. **Using the ResultSet getObject() Method**

The ResultSet getObject() method can be used to retrieve an Object from the ResultSet. This method will return null if the value is null. Therefore, it is possible to determine if a value is null using this method.

3. **Checking the Return Value**

When using the getObject() method, it is necessary to check the return value to determine if the value is null. This can be done by using an if statement to check if the returned Object is null.

4. **Example Code**

The following example code shows how to check for a null int value using the ResultSet getObject() method:

```java
int value = 0;
Object obj = resultSet.getObject("columnName");
if (obj != null) {
   value = (Integer) obj;
}
```
