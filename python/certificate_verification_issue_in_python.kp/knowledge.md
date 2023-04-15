---
title: Verification of certificate failed due to the inability to obtain the certificate of the issuing authority located locally
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: This error occurs when the SSL certificate on the server cannot be verified by the client because the client is unable to find the local issuer certificate.
---

**Contents**

[TOC]

### Overview

When making an HTTPS request in Python, you may encounter an error message like the following:

```
requests.exceptions.SSLError: HTTPSConnectionPool(host='example.com', port=443): Max retries exceeded with url: / (Caused by SSLError(SSLError("bad handshake: Error([('SSL routines', 'tls_process_server_certificate', 'certificate verify failed')])")))
```

This error occurs because Python was unable to verify the SSL/TLS certificate presented by the HTTPS server. In this guide, we'll look at some possible causes of this error and how to fix it.

### Potential Causes

#### Missing or Outdated CA Certificates

When Python connects to an HTTPS server, it needs to verify that the server's SSL/TLS certificate is trusted by a recognized certificate authority (CA). To do this, Python uses a set of CA certificates that are built into the system or provided by the user.

If these CA certificates are missing or out of date, Python won't be able to verify the server's certificate, resulting in the "certificate verify failed" error.

To check if this is the issue, you can try upgrading your Python version or manually adding the missing root certificates to your system.

#### Self-Signed or Invalid Certificates

If the SSL/TLS certificate presented by the HTTPS server is self-signed or has invalid attributes, Python may not be able to verify it. This could happen, for example, if you're connecting to a development server or a server with a misconfigured certificate.

You can try disabling certificate verification (not recommended for production use) or obtaining a valid certificate for the server.

### Possible Solutions

#### Option 1: Update Your CA Certificates

To update the CA certificates used by Python, you can try upgrading your Python version or manually installing the latest version of the `certifi` package:

```bash
pip install --upgrade certifi
```

This will install the latest set of CA certificates into your Python installation.

#### Option 2: Add Missing CA Certificates

If you're using a system-provided version of Python and the `certifi` package doesn't work, you can try manually adding the missing root certificates to your system.

On Debian/Ubuntu systems, you can install the `ca-certificates` package:

```bash
sudo apt-get install ca-certificates
```

On Red Hat/Fedora systems, you can install the `ca-certificates` package:

```bash
sudo yum install ca-certificates
```

#### Option 3: Disable Certificate Verification (Not Recommended)

If you know the server's certificate is trusted (e.g., if you're connecting to a local development server with a self-signed certificate), you can try disabling certificate verification in Python:

```python
import requests
from requests.packages.urllib3.exceptions import InsecureRequestWarning

requests.packages.urllib3.disable_warnings(InsecureRequestWarning)

response = requests.get("https://example.com", verify=False)
```

Note that this method is not recommended for production use and should only be used in development or testing environments.
