---
title: The git-upload-pack command could not be found when attempting to clone a remote git repository
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The command is not installed on the local machine, so it needs to be installed before cloning the remote Git repo.
---

**Contents**

[TOC]

## Overview
When attempting to clone a remote Git repository, the following error may be encountered: `git-upload-pack: command not found`. This error is usually caused by a missing or incorrect installation of Git on the local machine.

## Causes
The most common causes of this error are:

1. Git is not installed on the local machine.
2. The version of Git installed is outdated.
3. The PATH environment variable is not correctly configured to point to the location of the Git executable.

## Resolution
To resolve this issue, the following steps should be taken:

1. Ensure that Git is installed on the local machine.
2. Check the version of Git installed and make sure it is up-to-date.
3. Configure the PATH environment variable to point to the location of the Git executable.

## Conclusion
This error can be resolved by ensuring that Git is installed on the local machine, that it is up-to-date, and that the PATH environment variable is correctly configured to point to the location of the Git executable.
