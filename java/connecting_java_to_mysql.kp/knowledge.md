---
title: Establish a connection between Java and a MySQL database
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To connect Java to a MySQL database, use the JDBC driver.
---

**Contents**

[TOC]

### Install MySQL Connector/J
The first step to connecting Java to a MySQL database is to install the MySQL Connector/J, a JDBC driver that can communicate with MySQL databases. This can be done by downloading the driver from the [MySQL website](https://dev.mysql.com/downloads/connector/j/).

### Create a Database
The next step is to create a database that can be connected to from Java. This can be done using the MySQL command line client or using a GUI such as [MySQL Workbench](https://www.mysql.com/products/workbench/).

### Connect to the Database
Once the database has been created, it can be connected to from Java using the MySQL Connector/J. This can be done by creating a `Connection` object and passing in the necessary information such as the URL, username, and password.

### Execute Queries
Once the connection has been established, queries can be executed on the database. This can be done by creating a `Statement` object and executing the desired SQL query. The results of the query can then be retrieved and processed.
