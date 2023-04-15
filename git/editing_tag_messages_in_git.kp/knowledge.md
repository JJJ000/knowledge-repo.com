---
title: What is the process for modifying an existing tag message in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To edit an existing tag message in Git, use the `git tag -a` command with the `-m` option.
---

**Contents**

[TOC]

#1. Checkout the Tag
To edit an existing tag message in Git, you must first checkout the tag. This can be done by running the command `git checkout <tag_name>`. This will check out the tag and put you in a detached HEAD state. 

#2. Edit the Tag Message
Once the tag has been checked out, the tag message can be edited. This can be done by running the command `git tag -a -m <message> <tag_name>`. This will create a new tag with the specified message. 

#3. Push the Tag
Once the tag has been edited, it must be pushed to the remote repository. This can be done with the command `git push origin <tag_name>`. This will push the edited tag to the remote repository. 

#4. Verify the Tag
Once the tag has been pushed, it is important to verify that the tag has been updated. This can be done by running the command `git tag -v <tag_name>`. This will show the updated tag message and verify that the tag has been successfully updated.
