---
title: How to fix the error 'javax.net.ssl.sslhandshakeexception sun.security.validator.validatorexception pkix path building failed'?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The PKIX path building failed error is usually caused by a misconfigured or invalid SSL certificate.
---

**Contents**

[TOC]

### Causes

The javax.net.ssl.SSLHandshakeException is caused by a failure in the SSL handshake when trying to establish a secure connection. This is usually due to a misconfiguration or certificate issue.

### Troubleshooting

1. Check the server's SSL certificate to make sure it is valid and trusted.
2. Check the server's SSL configuration to make sure it is configured correctly.
3. Check the client's SSL configuration to make sure it is configured correctly.
4. Check the client's trust store to make sure the server's certificate is trusted.

### Resolution

1. If the server's SSL certificate is invalid or not trusted, obtain a valid certificate from a trusted Certificate Authority.
2. If the server's SSL configuration is incorrect, correct the configuration.
3. If the client's SSL configuration is incorrect, correct the configuration.
4. If the client's trust store does not contain the server's certificate, add the server's certificate to the trust store.

### Conclusion

SSLHandshakeException is usually caused by an invalid or untrusted SSL certificate or incorrect SSL configuration. To resolve the issue, make sure the server's SSL certificate is valid and trusted, and the server and client SSL configurations are correct. Additionally, make sure the server's certificate is added to the client's trust store.
