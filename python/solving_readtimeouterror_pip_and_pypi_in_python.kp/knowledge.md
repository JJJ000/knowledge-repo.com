---
title: What are the steps to address the issue of a readtimeouterror for httpsconnectionpool with pip while connecting to host 'pypi.python.org' on port 443?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: Increase the timeout value by using the `--default-timeout` parameter when running pip.
---

**Contents**

[TOC]

Section 1: Understanding the Error
The ReadTimeoutError: HTTPSConnectionPool(host='pypi.python.org', port=443) error is a common error encountered when using pip to install packages. This error occurs when pip fails to make a connection to the Python Package Index (PyPI) server over HTTPS, and the connection times out. The PyPI server is the default package repository for Python packages, and pip uses it to source packages for installation.

Section 2: Solutions to the Error
There are several solutions that can help resolve the ReadTimeoutError: HTTPSConnectionPool(host='pypi.python.org', port=443) error. Some of these solutions include:

1. Increasing Timeout: By default, pip waits for 15 seconds before timing out a connection. This timeout value can be increased by using the --default-timeout flag followed by the number of seconds you want to use. For example, to increase the timeout to 30 seconds, you can run the following command:
pip install --default-timeout=30 package_name

2. Disabling SSL Verification: Sometimes, the SSL certificate used by the PyPI server can cause connection issues. To resolve this, you can disable SSL verification by using the --trusted-host flag followed by the PyPI server's hostname. For example, to disable SSL verification for pypi.python.org, you can run the following command:
pip install --trusted-host pypi.python.org package_name

3. Using a Mirror: PyPI has several mirrors that can be used to download packages. These mirrors are often faster and more reliable than the main PyPI server. To use a mirror, you can add the URL of the mirror to the pip command using the --index-url flag. For example, to use the U.S. mirror, you can run the following command:
pip install --index-url https://mirrors.aliyun.com/pypi/simple/ package_name

4. Upgrading pip: An outdated version of pip can cause issues with connecting to the PyPI server. Upgrading pip to the latest version can help resolve this issue. You can upgrade pip by running the following command:
pip install --upgrade pip

Section 3: Conclusion
The ReadTimeoutError: HTTPSConnectionPool(host='pypi.python.org', port=443) error can be caused by several factors, including timeouts, SSL verification issues, outdated pip versions, and network issues. By using some of the solutions provided above, you can resolve the error and successfully install Python packages using pip.

Section 4: Additional Resources
- Official pip documentation: https://pip.pypa.io/en/stable/
- PyPI mirrors: https://pypi.org/mirrors/
- StackOverflow thread with similar issue: https://stackoverflow.com/questions/25973448/pip-install-throws-connection-error-ssl-certificate-verify-failed-certificate
