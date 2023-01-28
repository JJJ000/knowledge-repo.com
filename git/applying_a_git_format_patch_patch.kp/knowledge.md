---
title: What is the process for applying a patch created with git format-patch?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Apply the patch with the command `git apply <patch file>`.
---

**Contents**

[TOC]

### Generating the Patch

Before applying a patch, it must be generated. To generate a patch using Git, use the `git format-patch` command. This command takes a commit range as its argument and will generate a patch for each commit in the range. For example, to generate a patch for a single commit, use the following command:

```git
git format-patch -1 <commit hash>
```

### Preparing the Patch

Before applying the patch, it is important to ensure that the environment is ready for the patch. This includes making sure that the local repository is up-to-date with the remote repository and that any conflicts have been resolved.

### Applying the Patch

Once the patch is generated and the environment is ready, the patch can be applied. To apply the patch, use the `git am` command. This command takes a patch file as its argument and will apply the patch to the current branch. For example, to apply a patch file called `patch-file.patch`, use the following command:

```git
git am patch-file.patch
```

### Verifying the Patch

Once the patch is applied, it is important to verify that the patch was applied correctly. This can be done by running the `git log` command to view the commit history and ensuring that the patch has been applied correctly. It is also important to test the code to ensure that the patch does not introduce any new bugs.
