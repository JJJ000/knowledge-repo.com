---
title: What is the process for committing a new message without making any changes?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run `git commit --allow-empty -m `<message>`` to commit a new message with no change.
---

**Contents**

[TOC]

# Step 1: Create a New Commit

1. Check the status of your local repository: `git status`
2. Create a new commit: `git commit -m "Your message here"`

# Step 2: Push the Commit

1. Push the commit to your remote repository: `git push origin master`

# Step 3: Verify the Commit

1. Verify the commit has been pushed: `git log`
2. Verify the commit message: `git log --oneline`
