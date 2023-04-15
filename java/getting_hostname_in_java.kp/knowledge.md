---
title: The suggested method for obtaining a hostname in java
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The recommended way to get the hostname in Java is to use the InetAddress.getLocalHost().getHostName() method.
---

**Contents**

[TOC]

### java.net.InetAddress
The most recommended way to get a hostname in Java is to use the `java.net.InetAddress` class. This class provides methods to get the hostname of the local machine as well as any other host in the network.

### getHostName()
The `getHostName()` method of the `InetAddress` class can be used to get the hostname of the local machine. This method returns a string containing the hostname of the local machine.

### getByName()
The `getByName()` method of the `InetAddress` class can be used to get the hostname of any host in the network. This method takes a string containing the IP address of the host as an argument and returns an `InetAddress` instance containing the hostname of the specified host.

### getCanonicalHostName()
The `getCanonicalHostName()` method of the `InetAddress` class can be used to get the fully qualified domain name of the local machine. This method returns a string containing the fully qualified domain name of the local machine.
