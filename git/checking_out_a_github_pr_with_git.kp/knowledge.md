---
title: What is the process for using git to review a github pull request?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-04-18 00:00:00
updated_at: 2023-04-18 00:00:00
tldr: You can check out a GitHub pull request with git by using the `git checkout` command followed by the pull request branch name.
---

**Contents**

[TOC]

### Clone the Repository
1. Go to the repository page on GitHub.
2. Click the green "Clone or download" button.
3. Copy the URL that is displayed.
4. Open a terminal window and navigate to the directory where you want to clone the repository.
5. Run the following command: `git clone <URL>`

### Fetch the Pull Request
1. Change into the newly cloned repository directory.
2. Run the following command: `git fetch origin pull/<ID>/head:<BRANCHNAME>`
3. Replace <ID> with the pull request ID and <BRANCHNAME> with the desired branch name.

### Check Out the Pull Request
1. Run the following command: `git checkout <BRANCHNAME>`
2. Replace <BRANCHNAME> with the branch name used in the previous step.

### Push the Pull Request (Optional)
1. Run the following command: `git push origin <BRANCHNAME>`
2. Replace <BRANCHNAME> with the branch name used in the previous step.
