---
title: Add the server's self-signed ssl certificate to the Java client's truststore
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Yes, it is possible to accept a server`s self-signed SSL certificate in a Java client using the TrustManager class.
---

**Contents**

[TOC]

# Section 1: Overview

Java provides a variety of ways to accept a server's self-signed SSL certificate in a client application. This includes using a custom TrustManager, setting system properties, and setting up a custom SSLContext.

# Section 2: Custom TrustManager

The most secure way to accept a server's self-signed SSL certificate is to use a custom TrustManager. This allows the client to specify which certificates it will accept and which it will reject. The custom TrustManager can be set up using the javax.net.ssl.X509TrustManager interface. 

# Section 3: System Properties

Another way to accept a server's self-signed SSL certificate is to set system properties. This can be done by setting the javax.net.ssl.trustStore system property to point to a file that contains the server's self-signed certificate. The client will then use this file to validate the server's certificate.

# Section 4: Custom SSLContext

The last way to accept a server's self-signed SSL certificate is to set up a custom SSLContext. This can be done by creating an SSLContext object and setting the TrustManager to a custom TrustManager that will accept the server's self-signed certificate. The custom SSLContext can then be used when creating an SSL socket to connect to the server.
