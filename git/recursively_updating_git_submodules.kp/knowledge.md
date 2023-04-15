---
title: Recursively update git submodules
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To update submodules recursively, use the `git submodule update --recursive` command.
---

**Contents**

[TOC]

### Section 1 - Cloning a Repository with Submodules

When cloning a repository with submodules, you must use the `--recursive` option. This will ensure that all submodules are initialized and updated.

```git
git clone --recursive https://github.com/user/repo.git
```

### Section 2 - Updating Submodules

If you have an existing repository with submodules, you can update them by running the command `git submodule update --recursive` from the top-level of your repository. This will recursively update all submodules to the latest commit on their respective branches.

### Section 3 - Configuring Submodule Updates

You can configure your repository to update submodules automatically when you run `git pull` by adding the following to your `.git/config` file:

```git
[submodule "submodule_name"]
	url = https://github.com/user/repo.git
	update = recursive
```

### Section 4 - Submodule Status

If you want to check the status of your submodules, you can run the command `git submodule status` to see which commits each submodule is currently pointing to. This can be useful for ensuring that all submodules are up-to-date.
