---
title: Print the output of pprint by utilizing logging
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-16 00:00:00
updated_at: 2023-03-16 00:00:00
tldr: To use logging to print the output of pprint in Python, you can add the pprint output to the logging message and use the appropriate logging level to display the message.
---

**Contents**

[TOC]

## Introduction
Logging is an essential tool for debugging and understanding the flow of an application. It provides a way to track the execution of the program and save log messages to different targets, such as a file, console or email. Python comes with a built-in logging module that can be used to log pprint output.

## Importing the Required Modules and Configuring the Logging Module
To use the logging module in Python, we first need to import it. Along with the logging module, we also need to import the pprint module to generate formatted output.

```python
import logging
import pprint
```
Once the modules are imported, we need to configure the logging module to specify how the log messages will be handled. We can set the logging level, format the log messages and specify the log destination.

```python
logging.basicConfig(level=logging.DEBUG,
                    format='%(asctime)s %(name)s %(levelname)s %(message)s',
                    handlers=[logging.FileHandler('app.log', mode='w'),
                              logging.StreamHandler()])
```

## Logging the pprint output
To log the pprint output, we need to create a logger object using the logging.getLogger() method. We can then call the logger object's methods to write the pprint output to the log.

```python
logger = logging.getLogger(__name__)
data = {'name': 'John', 'age': 30, 'city': 'New York'}
logger.debug(pprint.pformat(data))
```
In the above code, we created a logger object with the same name as the current module. We then created a dictionary object and used pprint to format it. Finally, we pass the formatted data to the logger object's debug() method to write it to the log.

## Viewing the Log Messages
The log messages can be viewed in different ways, depending on the configuration. If we configured the logging module to write to a file, we can open the file to view the contents. If we sent the log messages to the console, we can check the console output. Here's an example of how to read the log messages from a file:

```python
with open('app.log', 'r') as f:
    print(f.read())
```

This will read the content of the 'app.log' file and print it to the console.

## Conclusion
In conclusion, we can use the pprint module to format complex data structures and log them using the logging module. This allows us to debug our applications and understand the program's behaviour at runtime. By logging the pprint output, we can capture the full context of our data and better understand the errors and exceptions in our application.
