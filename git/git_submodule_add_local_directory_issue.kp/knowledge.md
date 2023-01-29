---
title: What is the issue with using "git submodule add" to locate a git directory locally?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Run `git submodule update --init --recursive` to initialize and clone all submodules.
---

**Contents**

[TOC]

### Overview
Git submodule add is a command used to add a git repository as a submodule to an existing git repository. This command is often used to add a library or other code dependency to a project. However, sometimes when running the command, an error is thrown that states "a git directory is found locally". This error can be caused by a variety of issues, but the most common are related to the local repository structure.

### Causes
The most common cause of the "a git directory is found locally" error is that the local repository has not been set up correctly. When a repository is cloned from a remote repository, it is necessary to ensure that the local repository is properly configured. This includes setting up the correct remote URL and setting the local branch to track the remote branch. If these steps are not taken, the error can occur when attempting to add a submodule.

Another cause of the error is that the local repository is not up-to-date with the remote repository. If the local repository is not synced with the remote repository, the submodule may not be able to be added properly.

### Solutions
The first step to resolving the "a git directory is found locally" error is to ensure that the local repository is properly configured. This includes setting up the correct remote URL and setting the local branch to track the remote branch. Once this is done, the repository can be synced with the remote repository.

If the local repository is up-to-date with the remote repository, the next step is to check the git submodule configuration. This can be done by running the command `git submodule init` in the root directory of the repository. This will ensure that the submodule is properly configured and should resolve the error.

Finally, if all else fails, the last step is to delete the local repository and re-clone the remote repository. This will ensure that the local repository is properly configured and up-to-date with the remote repository, and should resolve the error.
