---
title: How do I undo the last commit in Git
authors:
- cool_wizard
tags:
- git
- knowledge
created_at: 2022-12-30 00:00:00
updated_at: 2022-12-31 21:44:24.406230
tldr: Use `git reset --soft HEAD~1` to undo the last commit and keep all the changes,
  or `git reset --hard HEAD~1` to clean up all the changes in the last commit.
---

**Contents**

[TOC]

### Look up the Git commit history

To view the commit history of a Git repository, you can use the `git log` command. By default, this command will show you a list of all commits in the repository, starting with the most recent commit:

```shell
git log
```

This will display the commit hashes, authors, dates, and commit messages for each commit in the repository.

You can also use various options to customize the output of `git log`. For example, the `--oneline` option will show the commits in a condensed format, with just the commit hash and the commit message on a single line:

```shell
git log --oneline
```

You can also use the `--author option` to filter the commits by author:

```shell
git log --author="John Doe"
```

### Undo the last commit

You can also use the `git reset` command to undo your last commit:

```shell
git reset --soft HEAD~1
```

The `--soft` option means that you will not lose the uncommitted changes you may have. To undo the latest commit, and also any uncommitted changes:

```shell
git reset --hard HEAD~1
```

### Reset to a particular commit

If you want to keep the changes made in the commit, but just move the branch pointer to the previous commit, you can use the `git reset` command with the `--soft` option:

```shell
git reset --soft <commit_hash>
```

This will move the branch pointer to the specified commit, but the changes made in the commit will remain in the working directory and can be committed again in a new commit.

To undo fully the most recent commit in Git, you can use the `git reset` command with the `--hard` option and specify the commit hash of the commit you want to revert to:

```shell
git reset --hard <commit_hash>
```

This will permanently remove the commit and any changes made in the commit from the repository. Be careful when using this option, as the changes are not recoverable.

It's also possible to use the `git revert` command to undo a commit. This creates a new commit that undoes the changes made in the previous commit, rather than permanently deleting the commit. To use git revert, specify the commit hash of the commit you want to undo:

```shell
git revert <commit_hash>
```

This is a safer option as it doesn't permanently destroy any commits, but it does add an additional commit to the repository's history.