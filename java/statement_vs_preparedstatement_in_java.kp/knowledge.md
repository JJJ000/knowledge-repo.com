---
title: The distinction between a statement and a preparedstatement is that a statement is used to execute a static sql statement, whereas a preparedstatement is used to execute a precompiled sql statement
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: A Statement is a basic SQL statement, while a PreparedStatement is a precompiled SQL statement that can contain parameters.
---

**Contents**

[TOC]

# Statement

A Statement object is used to execute a static SQL statement and return the results it produces. It is an interface which is used to execute a basic SQL statement.

# PreparedStatement

A PreparedStatement object is used for executing parameterized SQL statements. It is an interface which is used to execute a precompiled SQL statement.

# Key Differences

1. A Statement is used to execute a static SQL statement and return the results it produces, whereas a PreparedStatement is used for executing parameterized SQL statements.

2. A Statement is used to execute a basic SQL statement, whereas a PreparedStatement is used to execute a precompiled SQL statement.

3. A Statement is not suitable for precompiling SQL statements, whereas a PreparedStatement is suitable for precompiling SQL statements.

4. A Statement is not suitable for executing multiple SQL statements, whereas a PreparedStatement is suitable for executing multiple SQL statements.
