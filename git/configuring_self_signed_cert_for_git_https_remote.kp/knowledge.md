---
title: Set up git to recognize a specific self-signed certificate for a certain https remote
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run `git config http.sslCAInfo path/to/certificate` to configure Git to accept a particular self-signed server certificate for a particular https remote.
---

**Contents**

[TOC]

## Adding the Certificate

1. Download the self-signed certificate to the local machine. 
2. Add the certificate to the local trust store using the command `git config --global --add http.sslCAInfo <path to certificate>`

## Configuring Git

1. Configure Git to use the certificate for a specific remote using the command `git config --global http.https://<hostname>.sslCAInfo <path to certificate>`
2. Verify the configuration by running `git config --global --get-all http.https://<hostname>.sslCAInfo`

## Testing the Configuration

1. Try to fetch from the remote using the command `git fetch <remote>`
2. If the fetch is successful, the configuration was successful.
