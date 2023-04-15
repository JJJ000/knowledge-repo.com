---
title: The firewall blocked access to github over https due to the ssl certificate being rejected
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: If your firewall is blocking access to GitHub, you may need to configure it to allow access to GitHub`s servers and/or disable SSL certificate verification.
---

**Contents**

[TOC]

### Solution 1

1. Check with your corporate IT team to see if they have installed a corporate SSL certificate. If so, you should be able to access GitHub over HTTPS with no issues.

### Solution 2

1. If you are unable to access GitHub over HTTPS due to a firewall, you may be able to bypass the firewall by using a VPN. 
2. If you are unable to use a VPN, you may be able to access GitHub over an HTTP proxy. 
3. If you are unable to access GitHub over an HTTP proxy, you may be able to access GitHub over SSH. 
4. If you are unable to access GitHub over SSH, you may be able to access GitHub over a Tor connection.
