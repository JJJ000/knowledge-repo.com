---
title: Sync the git submodule to the most recent commit on the origin remote
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Run `git submodule update --remote` to update the submodule to the latest commit on origin.
---

**Contents**

[TOC]

1. Updating the Submodule
   - Change to the root directory of your local repository
   - Run `git submodule update --remote`

2. Committing the Change
   - Run `git add .`
   - Run `git commit -m "Updating submodule to latest commit"`

3. Pushing the Change
   - Run `git push origin master`

4. Verifying the Update
   - Change to the submodule directory
   - Run `git log` to see the latest commit
