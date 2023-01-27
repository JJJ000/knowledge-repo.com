---
title: You have not finished combining your changes (merge_head is still present)
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-27 00:00:00
updated_at: 2023-01-27 00:00:00
tldr: You must commit or reset the merge to conclude the merge.
---

**Contents**

[TOC]

### Resolve the Merge Conflict

The first step to resolving the merge conflict is to identify the source of the conflict. This can be done by running the command `git status`. This will provide a list of files with conflicts, which need to be resolved.

### Resolve the Conflicting Files

Once the source of the conflict is identified, the conflicting files must be opened and edited to resolve the conflict. Depending on the type of conflict, this may involve deleting conflicting lines, editing conflicting lines, or adding new lines. Once the conflict is resolved, the changes must be saved and committed.

### Commit the Resolved Merge

Once the conflicting files have been edited and saved, the resolved merge can be committed. This can be done by running the command `git commit -m "message"` where `message` is a description of the changes made.

### Push the Resolved Merge

The final step is to push the resolved merge to the remote repository. This can be done by running the command `git push origin master`. This will push the resolved merge to the remote repository, and the merge conflict will be resolved.
