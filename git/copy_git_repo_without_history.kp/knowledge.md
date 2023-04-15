---
title: Clone a git repository without past commits
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Clone the repo with the `--depth 1` flag to copy only the latest commit.
---

**Contents**

[TOC]

### Cloning the Repo

1. Open the terminal and navigate to the folder where you want to clone the repo.

2. Use the command `git clone --depth=1 <repo URL>` to clone the repo without its history.

### Verifying the Clone

1. Use the command `git log` to verify that the repo was cloned without its history.

2. If the log is empty, it means that the repo has been cloned without its history.
