---
title: What is the process for downloading from a git repository using an http proxy?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Use the `git config --global http.proxy` command to set the HTTP proxy for pulling from a Git repository.
---

**Contents**

[TOC]

### Configure Proxy

Before you can pull from a Git repository through an HTTP proxy, you must first configure your proxy settings. Depending on the type of proxy you are using, you will need to configure the proxy settings in your Git configuration file. For example, if you are using an HTTP proxy, you can configure your proxy settings by adding the following lines to your Git configuration file:

```git
[http]
	proxy = http://proxy.example.com:8080
```

You can also configure your proxy settings on the command line using the `git config` command. For example, if you are using an HTTP proxy, you can configure your proxy settings by running the following command:

```git
git config --global http.proxy http://proxy.example.com:8080
```

### Configure Authentication

If your proxy requires authentication, you will need to configure your authentication settings in your Git configuration file. Depending on the type of authentication required, you may need to configure your username and password, or an API token. For example, if you are using basic authentication, you can configure your authentication settings by adding the following lines to your Git configuration file:

```git
[http]
	proxy = http://proxy.example.com:8080
	proxyAuthMethod = basic
	proxyUser = username
	proxyPassword = password
```

You can also configure your authentication settings on the command line using the `git config` command. For example, if you are using basic authentication, you can configure your authentication settings by running the following command:

```git
git config --global http.proxy http://username:password@proxy.example.com:8080
```

### Pull from Repository

Once you have configured your proxy and authentication settings, you can pull from the repository by running the `git pull` command. For example, if you are pulling from a remote repository called `origin`, you can run the following command:

```git
git pull origin
```

### Verify Settings

Once you have pulled from the repository, you can verify your proxy and authentication settings by running the `git config --list` command. This will show you all of the configuration settings that are currently set in your Git configuration file.
