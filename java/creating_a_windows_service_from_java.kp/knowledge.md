---
title: What steps are necessary to turn a Java application into a windows service?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Create a Windows Service using the Apache Commons Daemon library.
---

**Contents**

[TOC]

# Section 1: Prerequisites
Before creating a Windows Service from a Java application, there are a few prerequisites that must be met.

- Java must be installed on the machine.
- The application must be packaged as a jar file.
- A service wrapper must be installed.

# Section 2: Install Service Wrapper
A service wrapper is a software that allows a Java application to be run as a Windows service. There are a few popular service wrappers available, such as Apache Commons Daemon, Tanuki Java Service Wrapper, and YAJSW.

# Section 3: Configure Service Wrapper
Once the service wrapper is installed, the next step is to configure it. This involves setting up the wrapper configuration file, which tells the service wrapper how to run the Java application as a Windows service.

# Section 4: Install and Run the Service
Finally, the service can be installed and started. This is done using the service wrapper command line utility, which takes the configuration file as an argument. Once the service is installed and started, it can be managed from the Windows Services Manager.
