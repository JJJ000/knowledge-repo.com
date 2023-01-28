---
title: What steps do I need to take to complete the merge after resolving the conflicts?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Once all conflicts have been resolved, run `git commit` to complete the merge.
---

**Contents**

[TOC]

#Commit Merge

After resolving all conflicts, a commit must be made in order to finalize the merge. This can be done by running the following command:

```git
git commit -m "Merge message"
```

#Push to Remote

Once the merge is committed, it must then be pushed to the remote repository. This can be done by running the following command:

```git
git push origin <branch-name>
```

#Verify Merged Changes

The final step is to verify that the merge was successful. This can be done by running the following command:

```git
git log --oneline --graph --decorate
```

This will show the commit history, including the newly merged commit. If the merge was successful, the commit history should show the two branches as having been merged.
