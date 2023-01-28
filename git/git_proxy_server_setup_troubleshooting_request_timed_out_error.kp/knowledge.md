---
title: Troubleshooting git to connect to a proxy server but receiving the error message "request timed out"
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Check the proxy settings in your git configuration to ensure they are correct.
---

**Contents**

[TOC]

### Setting Up Proxy

Before attempting to use Git with a proxy server, it is important to ensure that the proxy server is properly configured and that the correct proxy settings are applied. This can be done by setting the `HTTP_PROXY` environment variable to the correct proxy server address.

### Checking Connectivity

Once the proxy server is properly configured, it is important to check that the connection is working properly. This can be done by running a simple `curl` command to the proxy server address. If the connection is successful, the output should show that the request was successful.

### Troubleshooting

If the connection fails with a "Request timed out" error, it is likely that either the proxy server is not properly configured or the proxy settings are not properly applied. It is important to check both of these issues and make sure that they are properly addressed before attempting to use Git with a proxy server.

### Git Configuration

Once the proxy server is properly configured and the proxy settings are properly applied, it is important to configure Git to use the proxy server. This can be done by setting the `http.proxy` configuration option in the `.gitconfig` file. Once this is done, Git should be able to connect to the proxy server and the "Request timed out" error should no longer occur.
