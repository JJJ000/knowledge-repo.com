---
title: Using httpclient to trust all https certificates
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: HttpClient can be configured to trust all certificates by setting the SSLContext to use a TrustAllStrategy.
---

**Contents**

[TOC]

### Introduction

HTTPS is a secure version of the Hypertext Transfer Protocol (HTTP). It is used to establish an encrypted connection between a web server and a browser. HTTPS uses Transport Layer Security (TLS) or its predecessor, Secure Sockets Layer (SSL), to encrypt all communication between the two parties. As a result, any data exchanged between the two is kept private and secure.

In order to establish a secure connection, the web server must present a certificate to the browser. The browser then verifies the certificate to ensure that it is valid and trusted. If the browser does not trust the certificate, it will not establish the connection.

### HttpClient

HttpClient is a Java library that provides an API for making HTTP requests. It is used to send and receive data over the internet, such as web pages, images, and files. HttpClient supports both HTTP and HTTPS connections.

When making an HTTPS request, HttpClient needs to be configured to trust the server's certificate. If the certificate is not trusted, HttpClient will not be able to establish a secure connection.

### Trusting All Certificates

In some cases, it may be necessary to configure HttpClient to trust all certificates, regardless of whether they are valid or not. This can be done by creating a custom TrustManager that will always return true when verifying a certificate.

### Conclusion

In summary, HttpClient can be configured to trust all certificates using a custom TrustManager. This can be useful in certain situations, but it should be used with caution as it may expose the system to security risks.
