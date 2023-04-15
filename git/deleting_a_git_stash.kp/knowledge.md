---
title: What is the procedure for removing a stash created using git stash create?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: Run `git stash drop` followed by the stash id.
---

**Contents**

[TOC]

### View Stash 

1. Open the terminal and navigate to the directory containing the repository.
2. Enter the command `git stash list` to view the list of stashes.

### Delete Stash

1. Enter the command `git stash drop <stash_name>` to delete the specified stash.
2. Confirm the deletion by entering `y` when prompted.

### Confirm Deletion

1. Enter the command `git stash list` to confirm the deletion.
2. The deleted stash should no longer appear in the list.

### Remove References

1. Enter the command `git gc --prune=now` to remove any references to the deleted stash.
2. The deleted stash should now be completely removed from the repository.
