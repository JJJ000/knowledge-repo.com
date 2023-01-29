---
title: What is the difference between singletons and application context in android?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Singletons are used for global access to an object, while Application Context is used to store global application state.
---

**Contents**

[TOC]

#Singletons
A singleton is a design pattern where only a single instance of a class is created in the application. It is used when only one instance of a class is needed throughout the application. All instances of a singleton class share the same data, and methods can be called from any instance.

#Application Context
Application context is an Android-specific concept. It provides access to application-level information such as resources and activities. It also provides access to system services such as location and sensor services. It is often used to pass information between activities and services.
