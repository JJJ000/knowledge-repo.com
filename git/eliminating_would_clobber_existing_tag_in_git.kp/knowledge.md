---
title: What is the best way to remove the "would clobber existing tag" tag?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Run `git tag -f <tagname> <commit-sha>` to force the tag to the desired commit.
---

**Contents**

[TOC]

#1 Resolve Conflicts
If you are getting the "would clobber existing tag" error in Git, it means that you are trying to overwrite an existing tag in your repository. To get rid of this error, you must first resolve the conflict by either removing the existing tag or choosing a different name for your new tag.

#2 Delete Existing Tag
If you decide to delete the existing tag, you can do so by using the `git tag -d` command followed by the tag name. This will delete the existing tag and allow you to create a new tag with the same name.

#3 Change Tag Name
Alternatively, you can also choose to change the name of your tag to something else. This can be done by using the `git tag` command followed by the new tag name. This will create a new tag with the specified name, without overwriting the existing tag.

#4 Push Tag
Once you have resolved the conflict and created your new tag, you can push it to your remote repository using the `git push --tags` command. This will push all of your tags to the remote repository, including the new one that you just created.
