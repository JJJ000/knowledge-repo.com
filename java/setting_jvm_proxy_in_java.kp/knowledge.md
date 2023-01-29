---
title: What is the procedure for configuring the jvm to use a proxy?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: Set the `http.proxyHost` and `http.proxyPort` system properties.
---

**Contents**

[TOC]

### Setting the JVM Proxy

### Using Command Line Arguments

The JVM proxy can be set via command line arguments when starting the JVM. The `-Dhttp.proxyHost` and `-Dhttp.proxyPort` arguments can be used to specify the host and port of the proxy.

For example:

```
java -Dhttp.proxyHost=myproxy.example.com -Dhttp.proxyPort=8080 MyClass
```

### Using System Properties

The JVM proxy can also be set using Java system properties. The `http.proxyHost` and `http.proxyPort` system properties can be set in the program code before making any network connections.

For example:

```java
System.setProperty("http.proxyHost", "myproxy.example.com");
System.setProperty("http.proxyPort", "8080");
```

### Using Environment Variables

The JVM proxy can also be set using environment variables. The `HTTP_PROXY` and `HTTPS_PROXY` environment variables can be set to the host and port of the proxy.

For example:

```
export HTTP_PROXY=myproxy.example.com:8080
export HTTPS_PROXY=myproxy.example.com:8080
```
