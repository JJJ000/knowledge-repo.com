---
title: What is the process for searching through committed code in the git history using grep?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Use the `git log` command with the `-S` option to search the Git history for committed code.
---

**Contents**

[TOC]

### Using `git log`

The `git log` command can be used to search through the Git history for a particular string. To use it, simply pass the `--grep` flag with the string you'd like to search for:

```git
git log --grep="search string"
```

This will search through the commit message for the given string and return any commits that match.

### Using `git grep`

The `git grep` command is a more powerful version of `git log`. It can be used to search through the actual files in the repository for a particular string. To use it, pass the same `--grep` flag as before:

```git
git grep --grep="search string"
```

This will search through all of the files in the repository and return any matches.

### Using `git show`

The `git show` command can be used to view the contents of a particular commit. To use it, pass the commit hash of the commit you'd like to view:

```git
git show <commit_hash>
```

This will show the contents of the commit, including the diff of the changes that were made. You can then search through this diff for the string you're looking for.
