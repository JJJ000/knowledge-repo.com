---
title: Revert to the last committed state by using "git reset --hard" to discard any unsaved changes
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Git reset --hard will discard all uncommitted changes and reset the working directory to the last committed state.
---

**Contents**

[TOC]

### Introduction

Git reset --hard is a powerful command that can be used to recover from losing uncommitted changes. This command can be used to reset the working tree and index to the state of the HEAD commit, which means that all changes that have not been committed will be lost.

### How to Use Git Reset --Hard

Using git reset --hard is relatively straightforward. First, you need to make sure that you are in the correct branch. Then, you can run the command `git reset --hard` and it will reset the working tree and index to the state of the HEAD commit.

### Considerations

It is important to note that using this command will permanently delete any uncommitted changes, so it should be used with caution. Additionally, it is important to make sure that you are in the correct branch before running this command, as it will reset the entire branch.

### Conclusion

Git reset --hard is a powerful command that can be used to recover from losing uncommitted changes. When used correctly, it can be a useful tool in recovering from mistakes. However, it is important to use it with caution, as it can have unintended consequences if used incorrectly.
