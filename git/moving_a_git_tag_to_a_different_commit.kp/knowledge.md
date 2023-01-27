---
title: What is the process for transferring a tag on a git branch to a different commit?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: You can use the git tag command with the -f (force) option to move a tag to a different commit.
---

**Contents**

[TOC]

### Step 1: Checkout the Tag

To move a tag on a git branch to a different commit, the first step is to check out the tag. This can be done by running the command `git checkout <tag_name>`.

### Step 2: Move the Tag

The next step is to move the tag to the desired commit. This can be done by running the command `git tag -f <tag_name> <commit_id>`.

### Step 3: Push the Tag

The final step is to push the tag to the remote repository. This can be done by running the command `git push origin <tag_name> --force`. This will update the tag on the remote repository to the new commit.
