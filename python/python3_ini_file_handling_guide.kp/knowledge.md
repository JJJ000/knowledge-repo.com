---
title: What is the process of using python3 to read and write ini files?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: To read and write INI file with Python3, you can use the built-in configparser module.
---

**Contents**

[TOC]

## What is an INI file?

INI files are a type of configuration file that are commonly used to store settings and preferences for applications. The name INI stands for initialization.

An INI file typically consists of sections, each of which contains one or more key-value pairs. The values can be strings, integers, floats, or Booleans.

INI files are commonly used on Windows systems, where they are often used to store settings for applications and operating system components.


## Reading an INI file in Python3

Python provides a built-in module for handling INI files called "configparser". Here's how you can use it to read an INI file in Python3:

```python
import configparser

# Create a configparser object
config = configparser.ConfigParser()

# Load the INI file
config.read('path/to/file.ini')

# Access the values in the INI file
value = config.get('section', 'name')
```

In the example above, we first create a ConfigParser object. We then use its read method to load an INI file from disk.

To access a value in the INI file, we use the get method. We pass the name of the section that contains the value, followed by the name of the key.


## Writing to an INI file in Python3

To write to an INI file in Python3, we can use the ConfigParser object's set method. Here's an example:

```python
import configparser

# Create a configparser object
config = configparser.ConfigParser()

# Set a value in the INI file
config.set('section', 'name', 'value')

# Write the INI file to disk
with open('path/to/file.ini', 'w') as configfile:
    config.write(configfile)
```

In the example above, we first create a ConfigParser object. We then use its set method to set a value in the INI file.

Finally, we open a file object and call the ConfigParser object's write method to write the contents of the configparser object to the file.


## Handling errors while reading from an INI file in Python3

Reading from an INI file can result in errors if the file is not formatted correctly or if the requested section or key does not exist. The configparser module raises the NoSectionError and NoOptionError exceptions when an invalid section or option is requested.

Here's an example of how you can handle these errors:

```python
import configparser

# Create a configparser object
config = configparser.ConfigParser()

# Load the INI file
try:
  config.read('path/to/file.ini')
except configparser.Error as e:
  print('Error:', e)

# Access the values in the INI file
try:
  value = config.get('section', 'name')
except (configparser.NoSectionError, configparser.NoOptionError):
  print('Invalid section or option')
```


In the example above, we first load the INI file inside a 'try' statement. If any errors occur, we catch them and print an error message.

We then use another 'try' statement to retrieve a value from the INI file. If an invalid section or option is requested, we catch the appropriate exceptions and print an error message.
