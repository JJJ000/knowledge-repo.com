---
title: Get column names from java.sql.resultset
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The column names can be retrieved from a java.sql.ResultSet using the getMetaData() method.
---

**Contents**

[TOC]

### Using getMetaData
This is the most commonly used approach to retrieve the column names from a `java.sql.ResultSet`. It involves using the `ResultSet.getMetaData()` method to retrieve the `ResultSetMetaData` object, which contains information about the columns in the `ResultSet`.

### Example
The following code example shows how to use the `getMetaData()` method to retrieve the column names from a `ResultSet`:

```java
// Create a ResultSet object
ResultSet rs = stmt.executeQuery("SELECT * from table_name");

// Retrieve the ResultSetMetaData object
ResultSetMetaData rsmd = rs.getMetaData();

// Get the number of columns
int numCols = rsmd.getColumnCount();

// Get the column names; column indexes start from 1
for (int i=1; i<=numCols; i++){
    String colName = rsmd.getColumnName(i);
    System.out.println("Column " + i + ": " + colName);
}
```

### Using getColumnLabel
An alternative approach to retrieving the column names from a `ResultSet` is to use the `ResultSet.getColumnLabel()` method. This method returns the label of the specified column in the `ResultSet`.

### Example
The following code example shows how to use the `getColumnLabel()` method to retrieve the column names from a `ResultSet`:

```java
// Create a ResultSet object
ResultSet rs = stmt.executeQuery("SELECT * from table_name");

// Get the number of columns
int numCols = rs.getMetaData().getColumnCount();

// Get the column names; column indexes start from 1
for (int i=1; i<=numCols; i++){
    String colName = rs.getColumnLabel(i);
    System.out.println("Column " + i + ": " + colName);
}
```
