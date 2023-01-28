---
title: Git push --force-with-lease is different from --force in that it will only overwrite remote changes if the local branch is up to date with the remote branch. --force, on the other hand, will overwrite any remote changes regardless of whether the local branch is up to date
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: `git push --force-with-lease is a safer option than git push --force, as it ensures that the remote branch has not been updated since the last fetch.`
---

**Contents**

[TOC]

### --force-with-lease

`--force-with-lease` will check if the remote branch has been updated since the last time you fetched from it. If it has, the push will be rejected. This is useful for preventing you from accidentally overwriting someone else's work.

### --force

`--force` will override the remote branch and force the push, regardless of any changes that have been made since the last fetch. This can be dangerous, as it can overwrite someone else's work without warning.

### When to Use Each

`--force-with-lease` should be used when you are sure that the remote branch has not been updated since the last time you fetched from it. This is the safest option, as it will prevent you from accidentally overwriting someone else's work.

`--force` should only be used when you are absolutely sure that the remote branch has not been updated since the last time you fetched from it and that you want to override the remote branch, regardless of any changes that have been made since the last fetch. This is the least safe option, as it can overwrite someone else's work without warning.
