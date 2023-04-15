---
title: Searching for a specific word in git commit diffs or contents
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Run `git log -p -S <word>` to grep Git commit diffs or contents for a certain word.
---

**Contents**

[TOC]

### Grep Commit Diffs

To grep for a certain word in the commit diffs, you can use the following command:

```git
git log -p --word-diff=color --grep="<word>"
```

This command will search through the commit diffs and output the commits that contain the specified word.

### Grep Commit Contents

To grep for a certain word in the commit contents, you can use the following command:

```git
git log --grep="<word>"
```

This command will search through the commit contents and output the commits that contain the specified word.

### Grep for a Word in All Commits

To grep for a certain word in all commits (both diffs and contents), you can use the following command:

```git
git log --word-diff=color --grep="<word>"
```

This command will search through both the commit diffs and contents and output the commits that contain the specified word.

### Grep for a Word in a Specific Commit

To grep for a certain word in a specific commit, you can use the following command:

```git
git show --word-diff=color --grep="<word>" <commit-hash>
```

This command will search through the specified commit and output the parts of the commit that contain the specified word.
