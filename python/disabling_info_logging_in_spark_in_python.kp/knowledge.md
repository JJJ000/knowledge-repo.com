---
title: What is the process of disabling info logging in spark?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To turn off INFO logging in Spark in Python, set the log level to a higher level such as ERROR or WARNING using the following code sc.setLogLevel(`ERROR`).
---

**Contents**

[TOC]

## Introduction
In Spark, the logging level can be set using the `setLevel()` method of `Logger` class. The `Logger` class is part of the Python logging library. In order to turn off INFO logging, we need to set the logging level to a higher level than INFO, for example WARNING or ERROR.

## Checking current logging level
Before changing the logging level, we can check the current logging level using the following code snippet:

```python
import pyspark
import logging

sc = pyspark.SparkContext(appName="myAppName")

logger = logging.getLogger("py4j")
logger.setLevel(logging.ERROR)
```

Here, we import the PySpark library and the Python logging library. We create a new SparkContext with the name `myAppName`. We then create a logger object and set its logging level to ERROR.

## Setting the logging level
To turn off INFO logging, we can set the logging level to WARNING or ERROR. The following code snippet shows how to set the logging level to WARNING:

```python
import pyspark
import logging

sc = pyspark.SparkContext(appName="myAppName")

logger = logging.getLogger("py4j")
logger.setLevel(logging.WARNING)
```

This will set the logging level of the Py4J logger to WARNING. Since Spark uses the Py4J library for communication between the JVM and Python, this will also affect the logging level of Spark.

## Configuring logging at SparkConf level
Alternatively, you can configure logging at the `SparkConf` level. The `SparkConf` object allows you to set various configuration options for Spark, including the logging level. Here's how you can set the logging level to WARNING using `SparkConf`:

```python
import pyspark

conf = pyspark.SparkConf().setAppName("myAppName").set("spark.log.level", "WARN")
sc = pyspark.SparkContext(conf=conf)
```

Here, we create a `SparkConf` object with the app name `myAppName` and set the logging level to WARN using the `set` method. We then create a SparkContext object using the `SparkConf` object.

## Conclusion
In this tutorial, we learned how to turn off INFO logging in Spark in Python. We can set the logging level using the `setLevel()` method of the `Logger` class or by configuring the logging level at the `SparkConf` level.
