---
title: Retrieving a public key is not permitted when connecting Java to mysql
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Public Key Retrieval is not allowed in Java-MySQL Connections as it is not supported by the MySQL JDBC driver.
---

**Contents**

[TOC]

1. Overview
Public Key Retrieval is a feature that allows a client to retrieve the public key of the server it is connecting to. This is mainly used for secure connections like SSL/TLS. When connecting to a MySQL database using the JDBC driver, this feature is not allowed as it is not supported by the server.

2. How Does It Work?
When establishing a secure connection between two systems, the client needs to authenticate itself to the server. This is done by exchanging public keys. The client sends its public key to the server, which then sends its public key back to the client. This exchange of public keys is known as Public Key Retrieval.

3. Why Is Public Key Retrieval Not Allowed?
Public Key Retrieval is not allowed when connecting to a MySQL database using the JDBC driver because it is not supported by the server. This means that the server cannot send its public key to the client, and therefore the client cannot authenticate itself. 

4. Alternatives
If you need to establish a secure connection between a client and a MySQL database, you can use a third-party tool such as OpenSSL. OpenSSL provides an easy-to-use command-line interface that allows you to generate and exchange public keys. You can then use these public keys to authenticate the connection.
