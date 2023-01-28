---
title: What is the process for employing git bisect?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Git bisect is used to identify which commit introduced a bug in a codebase by binary searching through commits.
---

**Contents**

[TOC]

### Setup
1. Identify a commit that is known to work and a commit that is known to be broken.
2. Checkout the commit that is known to be broken.
3. Run `git bisect start` in the terminal.
4. Run `git bisect bad` to identify the current commit as the "bad" commit.
5. Run `git bisect good <known-good-commit-hash>` to identify the known-good commit as the "good" commit.

### Execution
1. Run `git bisect run <command>` to run a command (e.g., `npm test`) on each commit as git bisect moves through the commit history.
2. If the command returns an exit code of 0, the commit is "good"; if it returns a non-zero exit code, the commit is "bad".
3. After running the command, git bisect will move to the next commit in the history and repeat the process until it finds the commit that caused the issue.

### Cleanup
1. When git bisect has identified the commit that caused the issue, run `git bisect reset` to reset the repository back to the HEAD commit.
2. Run `git bisect log` to view the log of commits that were tested.
