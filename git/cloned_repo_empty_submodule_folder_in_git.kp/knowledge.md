---
title: When a repository is cloned, the associated git submodule folder will be empty
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: If a Git submodule is not initialized and updated when a repo is cloned, the submodule folder will be empty.
---

**Contents**

[TOC]

# Introduction

Git submodules are a powerful tool for managing repositories within a larger project. A submodule is essentially a repository within a repository. It allows a developer to include an external repository as part of their project, while still being able to manage it separately from the main repository.

# Empty Git Submodule Folder

When a repository is cloned, the submodule folder will be empty. This is because the submodule is not actually included in the repository, but is instead referenced from an external repository. The submodule folder will only contain the files and folders from the external repository if the submodule is initialized and updated.

# Initializing the Submodule

In order to have the submodule folder populated with the files from the external repository, the submodule must be initialized. This can be done by running the `git submodule init` command. This command will tell Git to look for the submodule in the external repository and initialize it.

# Updating the Submodule

Once the submodule has been initialized, it must be updated in order to have the files from the external repository added to the submodule folder. This can be done by running the `git submodule update` command. This command will fetch the latest version of the external repository and add the files to the submodule folder.

# Conclusion

In conclusion, when a repository is cloned, the submodule folder will be empty. This is because the submodule is not actually included in the repository, but is instead referenced from an external repository. The submodule folder will only contain the files and folders from the external repository if the submodule is initialized and updated.
