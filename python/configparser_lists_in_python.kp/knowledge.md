---
title: Configparser and its use of lists
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-16 00:00:00
updated_at: 2023-04-16 00:00:00
tldr: ConfigParser in Python can use lists as values by using the `split()` and `join()` methods to parse and serialize lists respectively.
---

**Contents**

[TOC]

Introduction:
Python has a built-in module called ConfigParser that allows us to easily parse configuration files. It supports having lists inside configuration files which can be very useful in various scenarios.

Section 1: Defining Lists in ConfigParser
To define lists in the configuration file, we need to enclose the list elements within square brackets [] and separate each element by a comma. 

For example:
```
[Numbers]
my_list = [1, 2, 3, 4, 5]
```
Here, we have defined a list called "my_list" with five elements using square brackets.

Section 2: Reading Lists in ConfigParser
To read the list from the configuration file in Python, we need to use the get() method of the ConfigParser object. 

For example:
```
import configparser

config = configparser.ConfigParser()
config.read('config.ini')

my_list = config.get('Numbers', 'my_list')
print(my_list)
```
This will output the entire list as a string including the square brackets and commas.

Section 3: Converting Lists to Python Lists
To convert the list string obtained from the configuration file into a Python list, we can use the ast module's literal_eval() function.

For example:
```
import configparser
import ast

config = configparser.ConfigParser()
config.read('config.ini')

my_list = ast.literal_eval(config.get('Numbers', 'my_list'))
print(my_list)
```
Here, we are first importing the ast module and then using the literal_eval() function to convert the string into a Python list.

Section 4: Modifying Lists in ConfigParser
To modify a list in the configuration file, we need to read the list, modify it and then write it back to the configuration file.

For example:
```
import configparser
import ast

config = configparser.ConfigParser()
config.read('config.ini')

my_list = ast.literal_eval(config.get('Numbers', 'my_list'))
my_list.append(6)  # add an element to the list

config.set('Numbers', 'my_list', str(my_list))

# write back to file
with open('config.ini', 'w') as config_file:
    config.write(config_file)
```
Here, we are first reading the list, modifying it, and then setting the new value using the set() method. Finally, we are writing the updated configuration back to the file.
