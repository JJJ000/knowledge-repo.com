---
title: What could be the reason behind receiving an importerror no module named apiclient.discovery error in my Python app engine application that uses the translate api?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: The required module for the Google API client library is missing.
---

**Contents**

[TOC]

## 1. Missing Module in App Engine Environment

One possible reason for the `ImportError: No module named apiclient.discovery` error when using the Translate API in a Python App Engine app is that the necessary module is missing from the App Engine environment. The `apiclient.discovery` module is part of the `google-api-python-client` library, which is typically installed using `pip` or `setuptools`. However, when deploying to App Engine, the library dependencies should be included in the `requirements.txt` file instead of relying on the `pip` or `setuptools` installation. 

## 2. Incorrect Library Version in requirements.txt

Another possible issue could be that the `google-api-python-client` library version downloaded by the App Engine environment does not include the `apiclient.discovery` module, either because it is an older version or a customized version. To resolve this issue, verify that the `google-api-python-client` library and version specified in the `requirements.txt` file matches the version expected by the code.

## 3. Incorrectly Configured API Client

The `ImportError: No module named apiclient.discovery` error can also occur if the `googleapiclient.discovery.build()` function is not called correctly when setting up the API client. This function creates a service object for interacting with the Translate API, and the absence of the `apiclient.discovery` module in this context suggests that the API client has not been configured properly. To resolve this issue, check that the arguments passed to the `build()` function are valid and that the service object is being created correctly.


## 4. Incompatible Operation Systems and Architectures

Another possible reason for this error is that the operation system and architecture that the libraries were installed do not match those of the system where it is deployed. For instance, you could have tried to install the libraries in a Windows system but your app is deployed in a Linux system. The solution is to ensure that the correct libraries and versions are installed in the correct system and architecture.
