---
title: Transferring a git repository to an svn server
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: To push an existing Git repository to SVN, use the `git svn` command.
---

**Contents**

[TOC]

### Prerequisites

- Git installed
- SVN installed
- Access to the remote SVN repository

### Cloning the Repository

1. Clone the existing Git repository:

```
git clone <repository-url>
```

2. Change into the repository directory:

```
cd <repository-name>
```

### Initializing the SVN Repository

1. Initialize the SVN repository:

```
svnadmin create <svn-repository-name>
```

2. Create a trunk, branches, and tags directory in the SVN repository:

```
svn mkdir <svn-repository-url>/trunk <svn-repository-url>/branches <svn-repository-url>/tags -m "Initial directory structure"
```

### Pushing to SVN

1. Push the Git repository to the SVN repository:

```
git svn init --prefix=origin/ <svn-repository-url>
git svn fetch
git push origin master:refs/remotes/trunk
```

2. Push the remaining branches and tags to the SVN repository:

```
git branch -r | grep -v '\->' | while read remote; do git branch --track "${remote#origin/}" "$remote"; done
git fetch --all
git push --all origin
git push --tags origin
```
