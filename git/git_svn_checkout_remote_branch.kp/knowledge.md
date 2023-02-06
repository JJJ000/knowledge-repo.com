---
title: Clone a remote branch using git svn
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To checkout a remote branch using git svn, use the command `git svn fetch` followed by `git checkout <branch\_name>`.
---

**Contents**

[TOC]

1. Clone the Remote SVN Repository

```
$ git svn clone [SVN repo URL]
```

2. Checkout a Remote SVN Branch

```
$ git checkout -b [branch_name] [SVN repo URL]/[branch_name]
```

3. Track the Remote SVN Branch

```
$ git svn branch -t [branch_name] [SVN repo URL]/[branch_name]
```

4. Update the Local Branch

```
$ git svn rebase
```
