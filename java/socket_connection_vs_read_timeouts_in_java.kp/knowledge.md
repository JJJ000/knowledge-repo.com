---
title: What is the distinction between the connection timeout and the read timeout when using sockets?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Connection timeout is the time to wait for a connection to be established, while read timeout is the time to wait for data to be read from an established connection.
---

**Contents**

[TOC]

#### Connection Timeout

Connection Timeout is the amount of time a socket waits for a connection to be established before timing out. This is important for applications which require a connection to be established within a certain amount of time. If the connection is not established within the timeout period, the socket will throw an exception and the connection will be terminated.

#### Read Timeout

Read Timeout is the amount of time a socket waits for data to be received before timing out. This is important for applications which require data to be received within a certain amount of time. If the data is not received within the timeout period, the socket will throw an exception and the connection will be terminated.
