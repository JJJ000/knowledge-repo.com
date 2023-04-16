---
title: The imported certificate is not providing a valid certification path to the requested target, resulting in an error
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The certificate may not be trusted by the target server, or the certificate may not be in the correct format.
---

**Contents**

[TOC]

# Section 1: Overview
When trying to establish a secure connection between a client and a server, the client must be able to verify the server's identity. This is done by having the server present a valid certificate that is signed by a trusted Certificate Authority (CA). If the client is unable to find a valid certification path to the requested target, the connection will fail with the error: "Unable to find valid certification path to requested target".

# Section 2: Possible Causes
There are several possible causes for this error. The most common are:
1. The server is not presenting a valid certificate that is signed by a trusted CA.
2. The client does not have the root CA certificate installed.
3. The client is not trusting the root CA certificate.

# Section 3: Solutions
1. Ensure that the server is presenting a valid certificate that is signed by a trusted CA.
2. Install the root CA certificate on the client.
3. Trust the root CA certificate on the client.

# Section 4: Conclusion
The error "Unable to find valid certification path to requested target" is typically caused by the client not having the necessary root CA certificate installed and/or trusted. To resolve this issue, the root CA certificate must be installed and trusted on the client.
