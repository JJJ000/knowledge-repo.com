---
title: After running filter-branch with the --tree-filter option, what is the process for removing refs/original/heads/master from the git repository?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The refs/original/heads/master reference will not exist after running filter-branch --tree-filter.
---

**Contents**

[TOC]

1. Before Removing Refs/Original/Heads/Master 
Before removing the refs/original/heads/master, it is necessary to understand what it is and how it affects the git repository. Refs/original/heads/master is a reference to the original commit of the repository. This reference is created when a filter-branch command is used to rewrite the history of the repository. This reference is used to ensure that the original commit is not lost in the rewriting process. 

2. Using Filter-Branch 
In order to remove the refs/original/heads/master reference, the filter-branch command needs to be used again. This command will rewrite the history of the repository and create a new reference to the original commit. The command should include the --prune-empty and --tree-filter flags. The --prune-empty flag will remove all empty commits created by the filter-branch command. The --tree-filter flag will modify the tree of the repository and delete the refs/original/heads/master reference. 

3. After Removing Refs/Original/Heads/Master 
After the refs/original/heads/master reference has been removed, the repository will no longer contain the original commit. The repository will only contain commits that were created after the filter-branch command was used. It is important to note that the original commit can still be accessed, but it is not part of the repository anymore. 

4. Conclusion 
Removing the refs/original/heads/master reference from a git repository after using the filter-branch command is a simple process. The filter-branch command needs to be used again with the --prune-empty and --tree-filter flags. This will rewrite the history of the repository and delete the refs/original/heads/master reference. After the reference has been removed, the repository will no longer contain the original commit.
