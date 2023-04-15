---
title: Retrieve results using the logging module in ipython notebook
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Use the command `logging.basicConfig(level=logging.DEBUG)` to get output from the logging module in IPython Notebook.
---

**Contents**

[TOC]

Introduction
------------

In IPython Notebook, the standard output and error can be easily captured and displayed in cell output. However, logging module output is not displayed in the same way. In this tutorial, we will see how to get the output from the logging module in IPython Notebook.


Importing logging module
------------------------

To use logging module, it must first be imported into the IPython Notebook environment using the below code:

```python
    import logging
```


Logging basic configuration
---------------------------

The basic configuration of logging module includes setting the logging level, setting the logging format, and selecting the output file. The below code snippet sets the logging level to DEBUG, sets the format to include timestamp, log level name and the message itself, and logs to the console output:

```python
    logging.basicConfig(level=logging.DEBUG, format='%(asctime)s - %(levelname)s - %(message)s')
```

Once this configuration is set, logging statements can be added throughout the code as needed, using the following code template:

```python
    logging.debug('This is a debug message')
    logging.info('This is an info message')
    logging.warning('This is a warning message')
    logging.error('This is an error message')
    logging.critical('This is a critical message')
```

Retrieving the logging output
------------------------------

By default, logging module sends all its output to the stderr object, which is not captured by IPython Notebook. To capture logging output in IPython Notebook, we can create a custom stream, which redirects logging messages to the IPython Notebook stdout stream. In this code snippet, I am creating a new stream handler that sends its output to STDOUT:

```python
    import sys
    sh = logging.StreamHandler(sys.stdout)
```

Now, we can add this new stream handler to the logging module using the code below:

```python
    logger = logging.getLogger()
    logger.addHandler(sh)
```

This tells logging module to use the custom stream handler we created earlier to output all logging messages.

Conclusion
----------

In this tutorial, we have seen how to get the output from the logging module in IPython Notebook. By creating a custom stream handler and adding it to the logging module, we can redirect the logging output to the IPython Notebook stdout stream, making it visible in cell output.
