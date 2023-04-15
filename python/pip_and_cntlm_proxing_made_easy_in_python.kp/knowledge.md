---
title: Employing cntlm to work with pip through a proxy
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: To use pip behind a proxy with CNTLM in Python, configure the proxy settings in the pip configuration file (pip.ini or pip.conf) to use the CNTLM server as the proxy.
---

**Contents**

[TOC]

Section 1: Introduction
-----------------------------
In some corporate environments or organizations, there is a proxy server between the network and the internet. This proxy server sits as an intermediary between your client and the actual server, allowing the client to request resources from the internet. However, configuring pip to work behind a proxy server can be challenging, especially if the proxy server requires authentication. In this tutorial, we will discuss how to configure pip to work behind a proxy with CNTLM in Python.


Section 2: Configuring CNTLM
-----------------------------
CNTLM is a proxy server that enables users to access the web when behind a proxy. In order to use CNTLM behind a proxy, first, download CNTLM from the official CNTLM website. After downloading, extract the package into a directory, and create a configuration file called cntlm.ini. Edit the configuration file and specify your proxy settings, including your username and password.

```
Username   username
Domain     yourdomain.com
Password   password
Proxy      10.0.0.150:3128
NoProxy    localhost, 127.0.0.*, 10.*, 192.168.*
Listen     127.0.0.1:3128
```

Save the cntlm.ini file and start running CNTLM by running the cntlm.exe command with administrator privileges.


Section 3: Configuring Pip
--------------------------
Once CNTLM is up and running, the next step is to configure pip to use the CNTLM proxy server. To do this, open a command prompt and type the following command:

```
pip install --proxy http://127.0.0.1:3128 packages
```

This command tells pip to use the CNTLM proxy server running on localhost port 3128. Replace "packages" with the name of the package you want to install.

If you want pip to always use CNTLM as a proxy server, you can add the following lines to your pip configuration file:

```
[global]
proxy = http://127.0.0.1:3128
```

This will configure pip to always use the CNTLM proxy server, which is running on localhost port 3128.


Section 4: Conclusion
----------------------
In conclusion, configuring pip to work behind a proxy server requires a bit of configuration, especially if your proxy server requires authentication. However, once you have CNTLM up and running, you can easily configure pip to use the CNTLM proxy server by specifying it in the command line or adding it to your pip configuration file. With these steps, you should be able to easily install Python packages with pip behind a proxy server.
