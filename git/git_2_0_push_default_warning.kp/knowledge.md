---
title: Be advised the default setting for 'push' is going to be different in git 2.0, so make sure it is set properly
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: Git 2.0 will default to the `simple` push behavior if push.default is unset.
---

**Contents**

[TOC]

### Implicit Value of Push.default

The implicit value of push.default is the current behavior of Git, which is to push the current branch to the branch with the same name on the remote.

### Changes in Git 2.0

In Git 2.0, the implicit value of push.default will be changed to `simple`. This means that Git will push the current branch to the branch with the same name on the remote, but will only push one branch at a time.

### Benefits of the Change

The change in the implicit value of push.default will make it easier to use Git because it will reduce the risk of accidentally pushing multiple branches at once.

### Recommendations

It is recommended that users of Git set the push.default configuration value to `simple`, or another value of their choosing, to ensure that they are using the desired behavior.
