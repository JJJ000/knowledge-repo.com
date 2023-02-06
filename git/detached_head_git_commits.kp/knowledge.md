---
title: What are the consequences of making git commits while in a detached head state?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: The commits will remain in the repository but will not be associated with any branch.
---

**Contents**

[TOC]

# Commits are Saved

When creating commits in a detached HEAD state, the commits are still saved to the repository. The commits will be stored in the repository and can be seen in the project's history.

# HEAD is Reattached

Once the detached HEAD state is resolved, the HEAD pointer will be reattached to the branch that it was previously on. This will allow the commits to be seen in the branch's history.

# Commits are Accessible

The commits created in a detached HEAD state are still accessible. They can be accessed through the project's history or by checking out the detached HEAD state.

# Commits are Visible

When viewing the project's history, the commits created in a detached HEAD state will be visible. The commits will show up in the project's history with the same information as any other commit.
