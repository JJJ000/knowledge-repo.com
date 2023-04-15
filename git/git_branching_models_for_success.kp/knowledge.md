---
title: Which git branching models are effective for you?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: Gitflow and GitHub Flow are both popular Git branching models that can work for many projects.
---

**Contents**

[TOC]

### Git Flow
Git Flow is a branching model that was created by Vincent Driessen. It is a popular model and is used by many teams. It defines two main branches, `master` and `develop`, and uses feature branches to manage new features and bug fixes. It also uses release branches to manage releases and hotfixes.

### GitHub Flow
GitHub Flow is a simpler branching model that was created by GitHub. It uses only a single `master` branch for production and releases, and uses feature branches for new features and bug fixes. It does not use release branches, instead opting for quick releases from `master`.

### GitLab Flow
GitLab Flow is similar to GitHub Flow, but uses two main branches, `master` and `develop`. It also uses feature branches for new features and bug fixes, and does not use release branches.

### GitLab-Forking Flow
GitLab-Forking Flow is a variation of the GitLab Flow model that uses forking instead of feature branches. It also uses two main branches, `master` and `develop`, and does not use release branches. It is a good option for teams who prefer to use forking instead of feature branches.
