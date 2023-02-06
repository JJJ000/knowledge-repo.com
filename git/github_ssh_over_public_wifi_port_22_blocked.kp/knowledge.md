---
title: Accessing github via ssh over a public wi-fi network where port 22 is blocked
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: It is not possible to connect to Github (SSH) via public WIFI if port 22 is blocked.
---

**Contents**

[TOC]

# Using a VPN

A Virtual Private Network (VPN) is the most reliable way to access Github (SSH) via public WIFI when port 22 is blocked. A VPN will encrypt your connection and tunnel your traffic through a secure tunnel, allowing you to bypass the port block.

# Using a Proxy

Another option is to use a proxy server. A proxy server is a computer system or application that acts as an intermediary between your computer and the Internet. It can be used to bypass port blocks by routing your traffic through a different port. However, this is not as secure as using a VPN, as the proxy server may be able to see your traffic.

# Using Tor

The Tor network is another option for accessing Github (SSH) via public WIFI when port 22 is blocked. Tor is a free, open-source network that routes your traffic through multiple nodes, making it difficult for anyone to trace your activity. However, it is not as secure as using a VPN, and it can be slow.

# Using SSH Tunneling

SSH tunneling is another option for accessing Github (SSH) via public WIFI when port 22 is blocked. SSH tunneling allows you to tunnel your traffic through a different port, bypassing the blocked port. However, this is not as secure as using a VPN or Tor, as the tunneling server may be able to see your traffic.
