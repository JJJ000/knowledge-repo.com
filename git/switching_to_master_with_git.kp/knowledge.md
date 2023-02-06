---
title: What is the command to return to the 'master' branch in git?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Run `git checkout master` to switch back to the `master` branch.
---

**Contents**

[TOC]

#1. Checkout the Master Branch

You can switch back to the master branch by running the following command:

```git checkout master```

#2. Pull from the Remote Repository

Next, you should pull from the remote repository to ensure your local master branch is up to date:

```git pull origin master```

#3. Verify the Branch

To verify that you have switched to the master branch, run the following command:

```git branch```

#4. Push to the Remote Repository

Finally, if you have made any changes to your local master branch, you should push them to the remote repository:

```git push origin master```
