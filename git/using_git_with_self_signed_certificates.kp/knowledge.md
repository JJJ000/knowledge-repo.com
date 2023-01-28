---
title: What steps do I need to take to make git recognize a self signed certificate?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: You can configure git to accept the self signed certificate by setting the environment variable GIT\_SSL\_NO\_VERIFY to true.
---

**Contents**

[TOC]

### Step 1: Add the Certificate to Your System

The first step is to add the self-signed certificate to your system. This can be done by saving the certificate to a file and then adding it to your system's list of trusted certificates.

### Step 2: Configure Git

The second step is to configure Git to accept the self-signed certificate. This can be done by setting the `sslVerify` option in your Git configuration to `false`.

### Step 3: Test the Connection

The third step is to test the connection to the server with the self-signed certificate. This can be done by running `git fetch` or `git clone` with the `--verbose` option to see if the connection succeeds.

### Step 4: Troubleshoot

If the connection fails, the fourth step is to troubleshoot the problem. This can be done by running `git fetch` or `git clone` with the `--trace` option to see the full details of the connection attempt.
