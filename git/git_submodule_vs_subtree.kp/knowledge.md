---
title: What are the distinctions between git submodule and subtree?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Git submodule is a separate repository that is linked to the main repository, while git subtree is a single repository with multiple components.
---

**Contents**

[TOC]

### Submodule

Submodules are a way of linking to a repository inside another repository. This allows developers to include the contents of one repository within another.

### Subtree

Subtrees are a way of including the contents of one repository within another. Unlike submodules, subtrees do not store their contents in a separate repository, but rather in the same repository as the parent project.

### Differences

1. Submodules require an extra step when cloning a repository, while subtrees do not.

2. Submodules are more difficult to update, as they require manual intervention. Subtrees can be updated with a single command.

3. Submodules are stored in a separate repository, while subtrees are stored in the same repository as the parent project.

4. Submodules are more difficult to merge, as they require manual intervention. Subtrees can be merged with a single command.
