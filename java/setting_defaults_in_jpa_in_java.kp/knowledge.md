---
title: Assigning default values to columns in jpa
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Default values can be set for columns in JPA by using the @Column annotation and setting the columnDefinition attribute.
---

**Contents**

[TOC]

### Setting Default Values in JPA

JPA provides the ability to set default values for columns in the database table. This can be done using the @Column annotation.

### Using the @Column Annotation

The @Column annotation is used to set the default value for a column. The @Column annotation has an attribute called "columnDefinition" which is used to set the default value. The syntax for setting the default value is as follows:

```
@Column(name = "COLUMN_NAME", columnDefinition = "DEFAULT_VALUE")
```

### Examples

Here are some examples of setting default values in JPA using the @Column annotation:

```
@Column(name = "is_active", columnDefinition = "boolean default true")
```

```
@Column(name = "created_at", columnDefinition = "timestamp default CURRENT_TIMESTAMP")
```

```
@Column(name = "status", columnDefinition = "varchar(20) default 'pending'")
```
