---
title: What is the procedure for taking out a submodule?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-26 00:00:00
updated_at: 2023-01-26 00:00:00
tldr: Run `git submodule deinit -f path/to/submodule` followed by `git rm -f path/to/submodule`.
---

**Contents**

[TOC]

### Step 1: Delete the relevant section from the .gitmodules file

The `.gitmodules` file contains a list of all the submodules associated with a particular repository. To delete a submodule, open the .gitmodules file and delete the relevant section. Make sure to save the file after making the changes.

### Step 2: Delete the relevant section from .git/config

The `.git/config` file contains a section for each submodule configured in the repository. To delete a submodule, open the .git/config file and delete the relevant section. Make sure to save the file after making the changes.

### Step 3: Run git rm --cached path_to_submodule

Run the following command to unregister the submodule from the repository:

```shell
git rm --cached path_to_submodule
```

### Step 4: Commit the change

Once the submodule has been unregistered, commit the changes to the repository. This will ensure that the changes are recorded and the submodule is removed from the repository.
