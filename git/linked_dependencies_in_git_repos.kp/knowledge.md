---
title: What steps do I need to take to establish linked dependencies in a git repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: You can use submodules in a git repo to link dependencies.
---

**Contents**

[TOC]

# 1. Submodules

Submodules are a way to include other git repositories within a parent repository. This allows the parent repository to track changes in the included repositories, while still allowing them to remain as separate entities.

# 2. Subtrees

Subtrees are a way to include a subtree of another repository into the current repository. Unlike submodules, subtrees do not require the included repository to be a separate git repository. This allows for more flexibility when linking between different projects.

# 3. Git Hooks

Git hooks are scripts that can be used to automate certain tasks when certain events occur. For example, a git hook can be used to automatically update a submodule when a commit is made in the parent repository.

# 4. Continuous Integration

Continuous Integration (CI) is a process in which changes in a repository are tested and integrated into the main codebase on a regular basis. This can be used to ensure that changes in linked repositories are tested and integrated into the main codebase in a timely manner.
