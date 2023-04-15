---
title: Unable to establish a link to your authorization agent
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Make sure your SSH agent is running and has your SSH key added.
---

**Contents**

[TOC]

### Troubleshooting
1. Ensure that the `ssh-agent` is running by typing `ps -e | grep ssh-agent` in the command line.
2. If the `ssh-agent` is not running, start it by typing `eval $(ssh-agent -s)` in the command line.
3. Add your SSH key to the `ssh-agent` by typing `ssh-add ~/.ssh/id_rsa` in the command line.
4. Verify that the SSH key has been added by typing `ssh-add -l` in the command line.
