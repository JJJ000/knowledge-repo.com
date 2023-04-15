---
title: What is the distinction between spi and api?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: SPI stands for Service Provider Interface and is a set of interfaces and classes that allow the application to extend its capabilities, while API stands for Application Programming Interface and is a set of functions and procedures that allow applications to access system services.
---

**Contents**

[TOC]

### SPI

* **Definition**: Service Provider Interface (SPI) is a mechanism to allow applications to use service implementations provided by different vendors.

* **Implementation**: SPI is implemented by creating a service provider interface and a service provider implementation. The service provider interface defines the methods that must be implemented by the service provider implementation. The application can then use the service provider interface to access the service provider implementation.

### API

* **Definition**: Application Programming Interface (API) is a set of routines, protocols, and tools for building software applications.

* **Implementation**: API is implemented by creating a set of classes and methods which can be used by the application to access the service provider implementation. The application can then use the API to access the service provider implementation.
