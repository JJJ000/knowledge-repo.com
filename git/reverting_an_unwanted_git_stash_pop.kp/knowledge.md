---
title: Reverting the changes made by an accidental git stash pop
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can undo an accidental git stash pop by using the git stash apply command to reapply the changes.
---

**Contents**

[TOC]

### Step 1: Stash the Unwanted Changes

The first step is to stash the unwanted changes. This can be done by running the following command:

```
git stash
```

### Step 2: Reset the Repository

The second step is to reset the repository to the desired state. This can be done by running the following command:

```
git reset --hard <commit-hash>
```

Where `<commit-hash>` is the commit hash of the desired state.

### Step 3: Apply the Stashed Changes

The third step is to apply the stashed changes. This can be done by running the following command:

```
git stash apply
```

### Step 4: Commit the Changes

The fourth and final step is to commit the changes. This can be done by running the following command:

```
git commit -m "Undo accidental git stash pop"
```
