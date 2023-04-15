---
title: What is the process for labeling an earlier commit in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-17 00:00:00
updated_at: 2023-04-17 00:00:00
tldr: To tag an older commit in Git, use the command `git tag <tagname> <commit\_id>`.
---

**Contents**

[TOC]

1. **Checkout the Commit:**
   To tag an older commit in Git, first checkout the commit you want to tag. To do this, use the command `git checkout <commit-id>` where `<commit-id>` is the identifier of the commit you want to tag.

2. **Create the Tag:**
   After you have checked out the commit, create the tag with the command `git tag <tag-name>`. This will tag the checked out commit with the tag name you specify.

3. **Push the Tag:**
   After creating the tag, push the tag to the remote repository with the command `git push <remote-name> <tag-name>`. This will push the tag to the remote repository.

4. **Verify the Tag:**
   Finally, verify that the tag was created successfully by running the command `git tag` to list all tags in the repository. The new tag should be listed in the output.
