---
title: What is the original source url of a local git repository that was cloned?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-26 00:00:00
updated_at: 2023-01-26 00:00:00
tldr: Run `git remote -v` to view the URL that the local Git repository was originally cloned from.
---

**Contents**

[TOC]

### Check the Config File

The easiest way to determine the URL that a local Git repository was originally cloned from is to check the config file of the repository. The config file contains information about the repository, including the URL from which it was cloned.

### Access the Config File

The config file can be accessed by navigating to the root directory of the repository and opening the `.git/config` file. This file is a plain text file and can be viewed with any text editor.

### Find the URL

Once the config file has been opened, look for the `url` line. This line will contain the URL from which the repository was originally cloned.

### Verify the URL

Once the URL has been found, it is important to verify that it is correct. This can be done by attempting to clone the repository again using the URL. If the clone is successful, the URL is correct.
