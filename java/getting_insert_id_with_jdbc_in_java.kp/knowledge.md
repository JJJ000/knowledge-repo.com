---
title: What is the method for retrieving the insert id using jdbc?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The insert ID can be retrieved using the ResultSet`s getGeneratedKeys() method.
---

**Contents**

[TOC]

`**` Create a Prepared Statement**

The first step to getting the insert ID in JDBC is to create a PreparedStatement object. This can be done using the `prepareStatement` method of the `Connection` class. The statement should include the `RETURN_GENERATED_KEYS` parameter, which will allow the JDBC driver to return any auto-generated keys.

`**` Execute the Statement**

Once the PreparedStatement object has been created, it can be executed using the `executeUpdate` method. This method will return the number of rows affected by the statement.

`**` Get the Generated Keys**

Once the statement has been executed, the generated keys can be retrieved using the `getGeneratedKeys` method of the `PreparedStatement` object. This method will return a `ResultSet` object containing the generated keys.

`**` Iterate Through the ResultSet**

The final step is to iterate through the `ResultSet` object and retrieve the insert ID. This can be done using the `next` and `getLong` methods of the `ResultSet` class. The `getLong` method will return the insert ID as a long value.
