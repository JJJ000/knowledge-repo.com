---
title: What is the process for setting git to use ssh as the default protocol for new repositories?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Set the `GIT\_PROTOCOL` environment variable to `ssh`.
---

**Contents**

[TOC]

### Setting Up SSH
1. Generate an SSH key pair on your local machine.
2. Add the public key to your Git provider's account settings.

### Configuring Git
1. Configure the Git global settings to use your SSH key.
2. Set the `url.ssh` variable to `git@github.com` in the global Git configuration.

### Testing the Setup
1. Try cloning a repository with `git clone git@github.com:username/repo.git`.
2. If the clone is successful, Git is now using SSH by default.
