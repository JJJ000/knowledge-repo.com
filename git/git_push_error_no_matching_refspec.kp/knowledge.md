---
title: The source reference specification 'master' does not match any when pushing commits in git
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-26 00:00:00
updated_at: 2023-01-26 00:00:00
tldr: This error occurs when the branch being pushed does not exist on the remote repository.
---

**Contents**

[TOC]

### Overview
When pushing commits to a remote repository, the message "src refspec master does not match any" is an indication that the local repository is not configured correctly with the remote repository. This message can be caused by a variety of issues, such as an incorrect remote repository URL, an incorrect branch name, or an incorrect configuration of the local repository. 

### Causes
1. Incorrect Remote Repository URL: If the local repository is configured with the wrong URL for the remote repository, the message "src refspec master does not match any" will be displayed. This can occur if the URL was entered incorrectly, or if the remote repository was moved to a different location. 

2. Incorrect Branch Name: If the local repository is configured with the wrong branch name for the remote repository, the message "src refspec master does not match any" will be displayed. This can occur if the branch name was entered incorrectly, or if the branch was renamed on the remote repository. 

3. Incorrect Configuration: If the local repository is not configured correctly, the message "src refspec master does not match any" will be displayed. This can occur if the remote repository is not configured correctly in the local repository, or if the local repository is not configured correctly with the remote repository. 

### Solution
The message "src refspec master does not match any" can be resolved by ensuring that the local repository is correctly configured with the remote repository. This can be done by verifying the URL, branch name, and configuration of the local repository. Once the configuration is correct, the commits should be able to be pushed to the remote repository without issue.
