---
title: Bypass git commit hooks
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Yes, you can bypass Git commit hooks by using the `--no-verify` flag.
---

**Contents**

[TOC]

### Pre-Commit Hooks

Git pre-commit hooks are scripts that are run before a commit is made. These hooks can be used to perform automated checks on the code, enforce coding standards, and prevent commits that do not meet certain criteria. This can be useful for ensuring quality control and preventing bugs from being committed to the repository.

### Skipping Pre-Commit Hooks

The pre-commit hooks can be skipped by using the `--no-verify` flag when running `git commit`. This flag will bypass the pre-commit hooks and allow the commit to be made without running the scripts.

### Post-Commit Hooks

Git post-commit hooks are scripts that are run after a commit is made. These hooks can be used to perform automated tasks such as sending notifications, running tests, and deploying code.

### Skipping Post-Commit Hooks

The post-commit hooks can be skipped by using the `--no-post-commit` flag when running `git commit`. This flag will bypass the post-commit hooks and allow the commit to be made without running the scripts.
