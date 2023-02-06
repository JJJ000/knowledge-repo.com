---
title: What is the command to make git pull overwrite all files on each pull?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run `git fetch --all; git reset --hard origin/<branch>` to force git pull to overwrite everything on every pull.
---

**Contents**

[TOC]

## Set Up

1. Navigate to the local repository on your machine.
2. Open the `.git/config` file.

## Configure

1. Add the following line to the file:

```
[branch "master"]
																																																																																																																																																																																																																																																																			remote = +refs/heads/*:refs/heads/*
force = true
```

## Execute

1. Execute `git pull` to force overwrite everything on every pull.
