---
title: Combine two git repositories while preserving the file history
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: The simplest way to merge two Git repositories without breaking file history is to use the `git merge-tree` command.
---

**Contents**

[TOC]

### Preparing the Repositories

Before merging the two Git repositories, a few steps must be taken to ensure that the file history is preserved. First, the two repositories should be cloned locally, and then the branches should be checked out. Additionally, the remote branches should be added and the repositories should be configured to push to the correct remote.

### Merging the Repositories

Once the repositories have been prepared, the next step is to merge the two repositories. This can be done by creating a new branch in one of the repositories and then merging the other repository into it. This will ensure that all of the changes from both repositories are preserved.

### Resolving Conflicts

Once the repositories have been merged, any conflicts that arise should be resolved. This can be done manually by editing the conflicting files and then committing them to the repository. Additionally, the Git command line can be used to resolve conflicts.

### Testing the Merged Repository

Finally, the merged repository should be tested to ensure that all of the changes were merged correctly. This can be done by running tests on the repository and verifying that all of the expected changes are present. Additionally, the Git log should be checked to ensure that all of the commits from both repositories are present.
