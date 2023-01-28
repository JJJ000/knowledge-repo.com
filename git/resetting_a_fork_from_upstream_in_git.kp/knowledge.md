---
title: Reset a fork to its original state and sync it with the original source
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: To clean up a fork and restart it from the upstream in Git, run `git fetch upstream` followed by `git reset --hard upstream/master`.
---

**Contents**

[TOC]

1. Delete the Forked Repository
  - Go to the repository page of the forked repository.
  - Click the Settings tab.
  - Scroll down to the Danger Zone and click Delete this repository.
  - Enter the repository's name and click I understand the consequences, delete this repository.

2. Re-Fork the Upstream Repository
  - Go to the upstream repository page.
  - Click the Fork button.
  - Select the account you want to fork the repository to.

3. Configure the Fork
  - Go to the forked repository page.
  - Click the Settings tab.
  - Scroll down to the Danger Zone and click Delete this repository.
  - Enter the repository's name and click I understand the consequences, delete this repository.

4. Sync the Fork with the Upstream
  - Go to the forked repository page.
  - Click the Settings tab.
  - Scroll down to the Danger Zone and click Delete this repository.
  - Enter the repository's name and click I understand the consequences, delete this repository.
  - Click the New pull request button.
  - Select the upstream repository as the base repository and the forked repository as the head repository.
  - Click Create pull request.
  - Merge the pull request.
