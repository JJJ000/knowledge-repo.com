---
title: What is the process for pushing to github using a different username?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can create a new SSH key and add it to your GitHub account under the new username.
---

**Contents**

[TOC]

# Configuring a Different Username

1. Open the Terminal and type `git config --global user.name "Your Name"` to set the new username you'd like to use.

2. Type `git config --global user.email "Your Email"` to set the new email address you'd like to use.

# Adding the New Credentials

1. Open the Terminal and type `git remote set-url origin git://new.url.here` to set the new URL for the remote repository.

2. Type `git push -u origin master` to push the changes to the remote repository.

# Verifying the New Credentials

1. Open the Terminal and type `git config --list` to verify the new username and email address are configured correctly.

2. Type `git remote -v` to verify the new URL is configured correctly.
