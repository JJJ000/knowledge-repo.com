---
title: Jenkins pipeline notserializableexception groovy.json.lazymap initialization failed
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: This exception occurs when an object is attempted to be serialized that is not serializable.
---

**Contents**

[TOC]

# Introduction
NotSerializableException is an exception that occurs when an object is not serializable. It is thrown when an object is not serializable, meaning it cannot be converted into a stream of bytes. In Jenkins Pipeline, this exception is thrown when an object is passed to a step that does not support serialization. In this article, we will discuss the NotSerializableException caused by groovy.json.internal.LazyMap.

# What is groovy.json.internal.LazyMap?
groovy.json.internal.LazyMap is a class that is used to parse JSON data. It is used to create a map from a given JSON string. The map is lazily evaluated, meaning that the values are not evaluated until they are accessed. This allows for faster parsing of large JSON strings.

# Causes of NotSerializableException
The NotSerializableException can be caused by passing a groovy.json.internal.LazyMap object to a step that does not support serialization. The object cannot be serialized, so the exception is thrown.

# Solutions
The best solution is to avoid passing a groovy.json.internal.LazyMap object to a step that does not support serialization. If this is not possible, then the object should be converted to a different type before it is passed to the step. This can be done using the toString() method or by using a custom serializer.
