---
title: A file containing properties in Python that is similar to the properties file in java
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Python supports a properties file format similar to Java Properties, allowing developers to store key-value pairs in a simple text-based format.
---

**Contents**

[TOC]

## Introduction

A properties file is a simple text file used to store key-value pairs. It is a popular way to store configuration information for applications. In Java, a properties file is commonly used to configure the application settings. Similarly, Python also provides a way to handle properties files to store configuration data.

## Python Properties

Python provides a library called `ConfigParser` to handle properties files. This library is similar to the `java.util.Properties` class in Java, which provides an easy way to read and write properties or settings from a file.

Here's an example of a simple properties file:

```ini
[database]
hostname=localhost
port=3306
username=myusername
password=mypassword
```

To work with this file in Python, we need to first create an instance of `ConfigParser` and then load the properties file into it. Here's some sample code:

```python
import configparser

config = configparser.ConfigParser()
config.read('config.ini')

# Read a value from the properties file
hostname = config.get('database', 'hostname')
```

In this example, we create an instance of `ConfigParser` and load the properties file `config.ini` into it. We can then read a value from the `database` section using the `get` method.

## Handling Defaults

One of the benefits of using a properties file is that it provides a default value for each configuration setting. In Python, we can set these default values using the `default` parameter of the `get` method.

For example, suppose we want to set a default value for the `port` setting in the `database` section. Here's how we can do it:

```python
import configparser

config = configparser.ConfigParser()
config.read('config.ini')

# Get the value of the port setting
# Use 3306 if the setting is not present
port = config.get('database', 'port', fallback=3306)
```

In this example, we use the `fallback` parameter to specify that the default value for the `port` setting should be `3306` if it's not present.

## Writing to a Properties File

In addition to reading from properties files, we can also write properties to a file using the same `ConfigParser` library. Here's an example of how we can write to a properties file:

```python
import configparser

config = configparser.ConfigParser()

# Set some configuration settings
config['database'] = {
    'hostname': 'localhost',
    'port': '3306',
    'username': 'myusername',
    'password': 'mypassword'
}

# Write the configuration to a file
with open('config.ini', 'w') as configfile:
    config.write(configfile)
```

In this example, we create an instance of `ConfigParser` and then set some configuration settings in the `database` section. We then write the configuration to a file using the `write` method. This will create a new properties file or overwrite an existing one with the same name.
