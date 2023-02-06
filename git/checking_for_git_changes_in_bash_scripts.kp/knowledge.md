---
title: What is the best way to determine if my local git repository has been modified using a bash script?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can check if your local Git repository has changes by running `git status` in a Bash script.
---

**Contents**

[TOC]

## Check for Changes

The following command can be used to check if there are any changes in the local Git repository:

```
git diff-index --quiet HEAD --
```

This command will return `0` if there are no changes, and `1` if there are changes.

## Check for Uncommitted Changes

To check if there are any uncommitted changes in the local Git repository, the following command can be used:

```
git status --porcelain
```

This command will return `0` if there are no changes, and `1` if there are changes.

## Check for Unpushed Changes

To check if there are any unpushed changes in the local Git repository, the following command can be used:

```
git log --branches --not --remotes
```

This command will return `0` if there are no changes, and `1` if there are changes.

## Bash Script

To use these commands in a Bash script, they can be combined with an `if` statement:

```
if [ $(git diff-index --quiet HEAD --) -eq 0 ] && [ $(git status --porcelain) -eq 0 ] && [ $(git log --branches --not --remotes) -eq 0 ]; then
    echo "No changes"
else
    echo "Changes detected"
fi
```
