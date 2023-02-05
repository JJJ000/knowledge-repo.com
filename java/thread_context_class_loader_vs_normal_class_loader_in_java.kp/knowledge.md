---
title: The difference between a thread's context class loader and a normal classloader is that the thread's context classloader is the classloader that the thread is associated with, while a normal classloader is any classloader that is not associated with a thread
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: The thread`s context class loader is used to dynamically load classes from other sources, while the normal class loader is used to load classes from the application`s classpath.
---

**Contents**

[TOC]

#1 Definition

Thread's Context Class Loader: The Thread's Context Class Loader is a class loader associated with each thread in the Java Virtual Machine (JVM). It is responsible for loading classes from the same class path as the thread's parent class loader.

Normal Class Loader: A normal class loader is a class loader responsible for loading classes from the class path. It is not associated with any thread in the JVM.

#2 Functionality

Thread's Context Class Loader: The Thread's Context Class Loader allows threads to have access to classes that are not visible to the parent class loader. This allows threads to dynamically load classes from different class paths.

Normal Class Loader: The Normal Class Loader is responsible for loading classes from the class path. It does not have any special functionality associated with it.

#3 Usage

Thread's Context Class Loader: The Thread's Context Class Loader is typically used when a thread needs to dynamically load classes from different class paths. This is useful when a thread needs to access classes that are not visible to the parent class loader.

Normal Class Loader: The Normal Class Loader is typically used when a thread needs to load classes from the class path. It is not typically used when a thread needs to access classes that are not visible to the parent class loader.

#4 Difference

Thread's Context Class Loader: The Thread's Context Class Loader allows threads to dynamically load classes from different class paths. This allows threads to access classes that are not visible to the parent class loader.

Normal Class Loader: The Normal Class Loader is responsible for loading classes from the class path. It does not have any special functionality associated with it and is not typically used when a thread needs to access classes that are not visible to the parent class loader.
