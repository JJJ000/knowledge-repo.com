---
title: Invoking Java code from python
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-15 00:00:00
updated_at: 2023-03-15 00:00:00
tldr: One can call Java from Python by using the Jython implementation which allows seamless integration of both languages.
---

**Contents**

[TOC]

Introduction
As two of the most popular programming languages, Java and Python are used extensively in the development of software applications. They offer unique features, functionalities and syntaxes that help developers achieve their intended objectives. Sometimes, a developer may want to call Java code from Python. In this article, we'll explore how to call Java from Python.

Using Jython
Jython is an implementation of the Python programming language that runs on the Java Virtual Machine. It allows Python code to interact with Java code, including importing Java classes and calling Java methods from Python. To use Jython, you need to have a Java Development Kit (JDK) installed on your system, which will provide the Java Runtime Environment (JRE) required to run Java code. With Jython, you can easily integrate Java code into your Python programs.

Using Py4J
Py4J is another library that allows you to call Java code from Python. It provides a gateway server that enables communication between Java and Python processes. To use Py4J, you need to install it using pip or any other package manager. Once installed, you can use it to instantiate Java objects, call Java methods, and access Java attributes from Python code. Py4J offers a simple and intuitive interface for Python developers to interact with Java code.

Conclusion
Calling Java from Python can be accomplished by using either Jython or Py4J. Both libraries offer an easy and powerful way to integrate Java code into your Python applications. While Jython runs Python code on the Java Virtual Machine, Py4J provides a gateway server that facilitates communication between Java and Python processes. Ultimately, the choice between these two libraries depends on your specific use case, and you should evaluate your requirements before choosing the one that best suits your needs.
