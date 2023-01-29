---
title: What is the process for applying a "git diff" patch without having git installed?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: You can apply a `git diff` patch using a patching tool such as patch(1).
---

**Contents**

[TOC]

### Using patch command

Patch command is a tool that can be used to apply a patch without having Git installed.

### Prerequisites

1. Install the patch command on your system.
2. Download the patch file from the Git repository.

### Steps

1. Navigate to the directory where the patch file is located.
2. Apply the patch using the following command:

```
patch -p1 < patch_file.diff
```

3. Check the changes with the following command:

```
git diff
```

4. Commit the changes using the following command:

```
git commit -m "Applied patch <patch_file_name>"
```
