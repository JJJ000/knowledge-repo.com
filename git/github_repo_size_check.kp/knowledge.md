---
title: What is the size of a github repository before I clone it?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: You can view the size of a GitHub repository by clicking on the `Clone or download` button and selecting `Download ZIP`.
---

**Contents**

[TOC]

### GitHub API
GitHub provides an API that can be used to view the size of a repository before cloning it. The API can be used to retrieve a repository's size in bytes by making a GET request to the `/repos/:owner/:repo` endpoint.

### GitHub GraphQL API
GitHub also provides a GraphQL API that can be used to view the size of a repository before cloning it. The API can be used to retrieve a repository's size in bytes by making a query to the `repository` endpoint.

### GitHub Web Interface
GitHub also provides a web interface that can be used to view the size of a repository before cloning it. The size of a repository can be found by navigating to the repository's homepage and viewing the size of the repository in the "Code" tab.
