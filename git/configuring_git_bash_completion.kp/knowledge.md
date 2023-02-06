---
title: What is the process for setting up git bash command line auto-completion?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Git bash command line completion can be enabled by running the `git-completion.bash` script.
---

**Contents**

[TOC]

## Section 1: Install Git Bash Completion

1. Download the git-completion.bash file from the [Git source repository](https://github.com/git/git/blob/master/contrib/completion/git-completion.bash).

2. Move the file to your home directory and rename it to .git-completion.bash

3. Open your .bashrc file in a text editor and add the following line:

```source ~/.git-completion.bash```

## Section 2: Configure Git Bash Completion

1. Open your .gitconfig file in a text editor and add the following lines:

```
[alias]
 # Enable tab completion
 c = config
 s = status
```

2. Add the following lines to your .bashrc file:

```
# Git tab completion
if [ -f ~/.git-completion.bash ]; then
  source ~/.git-completion.bash
fi
```

## Section 3: Test Git Bash Completion

1. Open a new terminal window and type in the following command:

```git c<tab>```

2. You should see the command autocomplete to ```git config```

## Section 4: Troubleshooting

1. If the autocomplete is not working, try running the following command:

```source ~/.bashrc```

2. If the issue persists, check the contents of your .bashrc and .gitconfig files to make sure they are properly configured.
