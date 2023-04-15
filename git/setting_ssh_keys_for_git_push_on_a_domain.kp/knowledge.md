---
title: Provide an ssh key for git push to a particular domain
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: The SSH key for git push for a given domain can be specified in the domain`s SSH configuration file.
---

**Contents**

[TOC]

1. Generate an SSH Key 

Generate an SSH key pair by running the following command in the terminal: 

`ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`

2. Add the SSH Key to the Domain

Add the SSH key to the domain by running the following command in the terminal:

`ssh-copy-id -i ~/.ssh/id_rsa.pub user@domain.com`

3. Configure Git

Configure git to use the SSH key by running the following command in the terminal:

`git config --global user.name "Your Name"`

`git config --global user.email "your_email@example.com"`

4. Push with SSH Key

Push to the domain using the SSH key by running the following command in the terminal:

`git push -u origin master`
