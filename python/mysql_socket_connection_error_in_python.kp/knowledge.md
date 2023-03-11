---
title: It is not possible to establish a connection to the local MySQL server using the '/tmp/mysql.sock' socket
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-11 00:00:00
updated_at: 2023-03-11 00:00:00
tldr: This error occurs when Python cannot connect to the MySQL server because the socket file `/tmp/mysql.sock` is either missing or has incorrect permissions.
---

**Contents**

[TOC]

# Understanding the error message

The error message "Can't connect to local MySQL server through socket '/tmp/mysql.sock" is an indication that the Python script is unable to establish a connection with the MySQL server due to a socket issue. 

The socket is a file that acts as an interface between the client and the MySQL server. It uses a specific file path to relay information between the two, and the error message suggests that the file path is either incorrect or inaccessible.

# Checking the MySQL server status

Before troubleshooting the error, it's essential to check if the MySQL server is running correctly. The following command can be used to check if the server is active:

```bash
sudo service mysql status
```

If the server is not running, the following command can be used to start it:

```bash
sudo service mysql start
```

# Verifying the socket file path

If the MySQL server is running fine, the next step is to verify the file path of the socket. The socket file path must be specified correctly in the Python code to establish a connection.

If the file path is incorrect, updating the code with the correct path should fix the error. 

```python
import mysql.connector
 
mydb = mysql.connector.connect(
  host="localhost",
  user="yourusername",
  password="yourpassword",
  database="mydatabase",
  unix_socket='/var/run/mysqld/mysqld.sock'
)
```

In this example, the file path for the socket is given as `/var/run/mysqld/mysqld.sock`. 

# Updating the MySQL configuration file

If the above steps do not work, the issue may be with the MySQL configuration file. The configuration file contains details on how the server operates and can be updated to fix the issue.

The MySQL configuration file is typically located in the `/etc/mysql/mysql.conf.d` directory. Once located, the following command is used to open and edit the file:

```bash
sudo nano /etc/mysql/mysql.conf.d/mysqld.cnf
```

In the configuration file, look for the `[mysqld]` section and add the following line to specify the location of the socket file:

```
socket=/var/run/mysqld/mysqld.sock
```

Save and exit the configuration file, then restart the MySQL service:

```bash
sudo service mysql restart
```

Try connecting to the MySQL server again using the Python script to verify if the issue is resolved.
