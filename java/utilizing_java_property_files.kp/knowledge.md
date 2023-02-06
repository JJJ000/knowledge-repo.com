---
title: What is the process for working with Java property files?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Java property files are used to store key-value pairs of configuration data which can be read and written using the java.util.Properties class.
---

**Contents**

[TOC]

# Section 1: What is a Java Property File?
A Java property file is a text file that contains data in key-value pairs. It is used to store configuration information, such as the database connection details, the application server settings, and other settings. The property file is loaded into the Java Virtual Machine (JVM) at startup time and is used to configure the application.

# Section 2: How to Create a Java Property File
Creating a Java property file is simple. All you need to do is create a text file with the .properties extension. The file should contain key-value pairs, with each pair separated by an equals sign (=). For example:

```
db.host=localhost
db.user=root
db.password=password
```

# Section 3: How to Load a Java Property File
To load a Java property file, you need to use the java.util.Properties class. This class provides methods to load the property file and access the values. Here is an example of how to load a property file:

```
Properties prop = new Properties();
FileInputStream in = new FileInputStream("config.properties");
prop.load(in);
```

# Section 4: How to Access a Java Property File
Once the property file is loaded, you can access the values using the getProperty() method. This method takes the key as an argument and returns the corresponding value. Here is an example of how to access a value from a property file:

```
String dbHost = prop.getProperty("db.host");
```
