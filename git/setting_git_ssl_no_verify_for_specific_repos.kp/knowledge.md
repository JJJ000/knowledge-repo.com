---
title: What is the procedure for configuring git_ssl_no_verify on specific repositories?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: You can set the GIT\_SSL\_NO\_VERIFY environment variable in the local repository`s .git/config file.
---

**Contents**

[TOC]

### Check Current Configuration

To check the current configuration of GIT_SSL_NO_VERIFY for a specific repository, run the command `git config --list --show-origin` from within the repository. This will show all the configuration options for the repository, including the setting for GIT_SSL_NO_VERIFY.

### Set Configuration

To set GIT_SSL_NO_VERIFY for a specific repository, run the command `git config --local http.sslVerify false` from within the repository. This will set the configuration option for GIT_SSL_NO_VERIFY to false for the repository.

### Verify Configuration

To verify that the configuration option for GIT_SSL_NO_VERIFY has been set correctly, run the command `git config --list --show-origin` from within the repository. This will show all the configuration options for the repository, including the setting for GIT_SSL_NO_VERIFY.

### Unset Configuration

To unset GIT_SSL_NO_VERIFY for a specific repository, run the command `git config --local --unset http.sslVerify` from within the repository. This will unset the configuration option for GIT_SSL_NO_VERIFY for the repository.
