---
title: Since upgrading to Java 1.7.0, an ssl handshake alert has been triggered with an 'unrecognized_name' error
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The `unrecognized\_name` error is caused by the server not recognizing the hostname used in the SSL handshake, and can be fixed by setting the `jsse.enableSNIExtension` system property to `false`.
---

**Contents**

[TOC]

# Introduction

Java 1.7.0 introduced a new security feature called the Server Name Indication (SNI) extension, which is an extension to the TLS protocol that allows the client to specify which server name it is connecting to during the SSL handshake process. This allows the server to present a different certificate depending on the server name that the client is connecting to.

# Unrecognized_name Error

When the SNI extension is enabled, the server may return an "unrecognized_name" alert if the server name that the client specified does not match the server name on the certificate. This can happen if the server is configured to use a wildcard certificate that covers multiple server names, but the client is connecting to a server name that is not covered by the certificate.

# Resolution

To resolve this issue, the server should be reconfigured to use a certificate that covers the server name that the client is connecting to. Alternatively, the client can be configured to not send the SNI extension during the SSL handshake process, which will prevent the server from returning the "unrecognized_name" alert.
