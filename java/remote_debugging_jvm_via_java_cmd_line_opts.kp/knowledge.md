---
title: Which command line options for Java should be set to enable remote debugging of the jvm?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: The Java command line options to set to allow JVM to be remotely debugged are `-Xdebug -Xrunjdwptransport=dt\_socket,server=y,suspend=n,address=<port\_number>`.
---

**Contents**

[TOC]

1. ##Enabling Debugging

To enable debugging on the JVM, you need to specify the following command line option:

`-agentlib:jdwp=transport=dt_socket,server=y,suspend=n,address=<debug-port>`

2. ##Debug Port

The debug port is a port number that the JVM will bind to in order to accept incoming debugging connections. It can be any unused port number.

3. ##Remote Debugging

To enable remote debugging, the debug port must be accessible from the remote machine. This can be done by either opening the port in the firewall, or by using SSH port forwarding.

4. ##Connecting to the Debugger

Once the debug port is accessible, a debugger can connect to it using the same port number. The debugger will then be able to control the execution of the JVM and inspect its state.
