---
title: What is the refspec for pushing a git tag to a branch?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: To push a Git tag to a branch using a refspec, use the command `git push <remote> <tagname><branchname>`.
---

**Contents**

[TOC]

#### Step 1: Tag the Commit

To push a Git tag to a branch, the commit must first be tagged. This can be done with the following command:

```
git tag <tagname> <commit>
```

Where `<tagname>` is the name of the tag and `<commit>` is the commit to tag.

#### Step 2: Push the Tag

Once the commit has been tagged, the tag can be pushed to the branch using the following command:

```
git push <remote> <tagname> --force
```

Where `<remote>` is the name of the remote repository and `<tagname>` is the name of the tag.

#### Step 3: Create a Refspec

A refspec is a special format for specifying a ref (or a tag) to push to a remote repository. The refspec for pushing a tag to a branch can be created with the following command:

```
git push <remote> <tagname>:refs/heads/<branchname> --force
```

Where `<remote>` is the name of the remote repository, `<tagname>` is the name of the tag, and `<branchname>` is the name of the branch.

#### Step 4: Push the Refspec

Finally, the refspec can be pushed to the branch with the following command:

```
git push <remote> <refspec> --force
```

Where `<remote>` is the name of the remote repository and `<refspec>` is the refspec created in the previous step.
