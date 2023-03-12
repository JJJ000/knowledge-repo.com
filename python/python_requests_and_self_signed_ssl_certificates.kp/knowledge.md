---
title: What are the steps to make Python requests trust a self-signed ssl certificate?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Pass the path to the self-signed certificate to the `verify` parameter when making a request using the requests library in Python.
---

**Contents**

[TOC]

# Introduction

Using self-signed SSL certificates is not recommended as they don't provide a trustworthy source of identity. However, in some cases, developers may need to use self-signed SSL certificates. One such case might be when testing a web application that uses HTTPS. This article will provide steps to get Python requests to trust a self-signed SSL certificate.

# Step 1: Generating a self-signed SSL certificate

To generate a self-signed SSL certificate, you can use the OpenSSL command-line tool. Here's how to generate a self-signed SSL certificate using OpenSSL:

1. Open Terminal/Command prompt.
2. Type in the following command: `openssl req -x509 -newkey rsa:4096 -nodes -out cert.pem -keyout key.pem -days 365`
3. Press Enter.
4. OpenSSL will prompt you to enter some information. You don't need to enter any valid information as this is a self-signed certificate.
5. After OpenSSL generates the certificate, it will save it to the current directory.

# Step 2: Adding the self-signed SSL certificate to the trusted certificate store

To get Python requests to trust a self-signed SSL certificate, you need to add the certificate to the trusted certificate store. Here's how to add the certificate to the trusted certificate store:

1. Open Terminal/Command prompt.
2. Type in the following command: `openssl x509 -in cert.pem -out cert.crt`
3. Press Enter.
4. Copy the cert.crt file to the trusted certificate store directory.
   - On macOS, the directory is `/Library/Python/2.7/site-packages/certifi/cacert.pem`.
   - On Windows, the directory is `C:\Python27\Lib\site-packages\certifi\cacert.pem`.
5. Open the cacert.pem file in a text editor.
6. Append the contents of the cert.crt file to the end of the cacert.pem file.
7. Save the cacert.pem file.

# Step 3: Using Python requests with a self-signed SSL certificate

After adding the self-signed SSL certificate to the trusted certificate store, you can now use Python requests with a self-signed SSL certificate. Here's an example code:

```python
import requests

url = "https://example.com"
response = requests.get(url, verify=True)
print(response)
```

In the example code above, the `verify` parameter is set to `True`. This tells requests to verify the SSL certificate. Since the SSL certificate is now in the trusted certificate store, requests will trust the SSL certificate and the code will run without error.

# Conclusion

Using self-signed SSL certificates is not recommended, but in some limited cases, developers may have to use them. In this article, we provided steps to get Python requests to trust a self-signed SSL certificate. However, it's always recommended to use SSL certificates from trusted certificate authorities to ensure safety and security.
