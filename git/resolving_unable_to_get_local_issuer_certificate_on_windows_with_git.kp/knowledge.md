---
title: Troubleshooting "unable to get local issuer certificate" when using git on windows with a self-signed certificate
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Ensure that the self-signed certificate is added to the Windows Certificate Store.
---

**Contents**

[TOC]

### Overview

The "unable to get local issuer certificate" error is a common issue encountered when using Git on Windows with a self-signed certificate. This error occurs when the certificate used for authentication is not trusted by the Git client. In order to resolve this issue, the certificate must be added to the Git client's list of trusted certificates.

### Understanding the Issue

When using Git on Windows with a self-signed certificate, the error "unable to get local issuer certificate" is encountered when the certificate used for authentication is not trusted by the Git client. This is because the Git client needs to be able to authenticate the certificate in order to establish a secure connection. If the certificate is not trusted, the connection will not be established and the error will be displayed.

### Resolving the Issue

In order to resolve the "unable to get local issuer certificate" error, the certificate must be added to the Git client's list of trusted certificates. This can be done by using the command line tool `git-credential-store`. This tool will allow the user to add the certificate to the list of trusted certificates.

### Conclusion

By understanding the issue and taking the necessary steps to add the certificate to the Git client's list of trusted certificates, the "unable to get local issuer certificate" error can be resolved. This will allow the user to successfully establish a secure connection with the Git server and use Git on Windows with a self-signed certificate.
