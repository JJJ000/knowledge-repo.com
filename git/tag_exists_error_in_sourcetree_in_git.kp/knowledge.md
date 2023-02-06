---
title: When trying to push in sourcetree, the updates were not accepted because the tag already existed
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The push was rejected because the tag being pushed already exists in the remote repository.
---

**Contents**

[TOC]

# Overview 
When attempting to push in SourceTree in Git, the error message "Updates were rejected because the tag already exists" may appear. This error indicates that the tag that is being pushed already exists in the remote repository, and therefore cannot be pushed again. 

# Causes
This error is caused by attempting to push a tag that already exists in the remote repository. This can occur if the tag has already been pushed from another local repository, or if the tag is being pushed from the same local repository that it was previously pushed from. 

# Solutions
The best way to resolve this issue is to delete the tag from the remote repository and then push the tag again. To delete the tag, use the command `git push --delete <remote_name> <tag_name>`. Once the tag has been deleted, the tag can be pushed again using the command `git push <remote_name> <tag_name>`. 

Alternatively, if the tag is not needed in the remote repository, it can simply be removed from the local repository. To remove the tag from the local repository, use the command `git tag -d <tag_name>`. Once the tag has been removed from the local repository, it can be pushed without issue.
