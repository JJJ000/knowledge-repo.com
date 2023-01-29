---
title: What is the process for outputting a query string with its associated parameter values when using hibernate?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Hibernate can print a query string with parameter values by using the toString() method on a Query object.
---

**Contents**

[TOC]

### Setting Up Logging

In order to print a query string with parameter values when using Hibernate in Java, the first step is to set up logging. This can be done by adding the following lines of code to the application's `log4j.properties` file:

```java
log4j.logger.org.hibernate.type=trace
log4j.logger.org.hibernate.SQL=debug
```

### Enabling Show_SQL

The next step is to enable the `show_sql` property in the application's `hibernate.cfg.xml` file. This can be done by adding the following line of code:

```java
<property name="show_sql">true</property>
```

### Setting Format_SQL

The third step is to set the `format_sql` property in the application's `hibernate.cfg.xml` file. This can be done by adding the following line of code:

```java
<property name="format_sql">true</property>
```

### Verifying Logs

Finally, the application's logs can be checked to verify that the query string with parameter values is being printed. This should be printed in the log file with a `DEBUG` level.
