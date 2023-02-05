---
title: What is the difference between using @notnull and @column(nullable = false) when working with jpa and hibernate?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: @NotNull is a Java annotation used to indicate that a variable should not be null, while @Column(nullable = false) is used to indicate that a column in a database table should not be null.
---

**Contents**

[TOC]

1. ##@NotNull
@NotNull is a Java annotation used to indicate that a method parameter or class field must not be null. It is a part of the javax.validation package and can be used to validate the state of an application.

2. ##@Column(nullable = false)
@Column(nullable = false) is a JPA annotation used to indicate that the corresponding column in the database table cannot contain null values. It is a part of the javax.persistence package and can be used to define the schema of the database table.

3. ##Differences
The main difference between the two annotations is that @NotNull is used to validate the state of an application while @Column(nullable = false) is used to define the schema of the database table.

4. ##Uses
@NotNull is used to validate the state of an application while @Column(nullable = false) is used to define the schema of the database table. In addition, @NotNull can be used to validate method parameters and class fields while @Column(nullable = false) can only be used to define database columns.
