---
title: When trying to serialize JSON in python, the error "typeerror (integer) is not JSON serializable" is thrown when an integer value is not able to be serialized
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-08 00:00:00
updated_at: 2023-02-08 00:00:00
tldr: The value being serialized must be a valid JSON type, such as a string, number, boolean, list, or dictionary.
---

**Contents**

[TOC]

#Section 1: What is JSON?
JSON (JavaScript Object Notation) is a lightweight data-interchange format. It is a text-based format that is used to store and exchange data between different systems. It is language independent, meaning it can be used with any programming language.

#Section 2: What is Serialization?
Serialization is the process of converting a data structure or object into a sequence of bits so that it can be stored in a file or memory buffer, or transmitted across a network connection link. In Python, serialization is achieved by using the json module.

#Section 3: What is TypeError?
TypeError is an exception raised when an operation or function is applied to an object of an inappropriate type. In the case of serializing JSON in Python, TypeError is raised when an object of an inappropriate type (such as Integer) is encountered.

#Section 4: How to Resolve TypeError?
In order to resolve TypeError, the object must be converted to an appropriate type before serializing it. For example, if an Integer is encountered, it must be converted to a String before serializing it.
