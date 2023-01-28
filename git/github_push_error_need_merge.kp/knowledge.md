---
title: I'm unable to upload my changes to github; it keeps telling me I need to merge
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: You may need to pull from GitHub and merge your changes before pushing.
---

**Contents**

[TOC]

### Overview
GitHub is a web-based hosting service for version control using Git. When attempting to push changes to a repository, a merge may be required if the remote repository has been updated since the last time it was pulled.

### Reasons for Merge Requirement
When pushing changes to a repository, the remote repository must be up-to-date with the local repository. If the remote repository has been updated by another user since the last time the local repository was updated, a merge will be required. This ensures that the changes from both repositories are included in the final version.

### How to Merge
To merge changes from the remote repository with the local repository, the user must first pull the changes from the remote repository. This can be done by running the `git pull` command. Once the changes have been pulled, the user can then run the `git merge` command to combine the changes from both repositories.

### Resolving Conflicts
In some cases, there may be conflicts between the changes from the two repositories. If this occurs, the user must manually resolve the conflicts before the merge can be completed. This can be done by opening the conflicting files and manually editing them to include the desired changes. Once the conflicts have been resolved, the user can then run the `git add` and `git commit` commands to commit the changes.
