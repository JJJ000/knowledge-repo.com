---
title: What portion of a git sha is typically required to pinpoint a modification in a specific codebase?
authors:
- know_how
tags:
- git
- knowledge
thumbnail: images/git.png
created_at: 2023-01-28 00:00:00
updated_at: 2023-01-28 00:00:00
tldr: Generally, a full 40-character git sha is necessary to uniquely identify a change in a given codebase.
---

**Contents**

[TOC]

1. Short SHA:
   Generally, the first 7 characters of a Git SHA are considered necessary to uniquely identify a change in a given codebase.

2. Long SHA:
   For a more secure and reliable identification, the full 40 characters of a Git SHA can be used.

3. Other Identifiers:
   In addition to the Git SHA, other identifiers such as commit message, author, timestamp, and branch can also be used to uniquely identify a change in a codebase.

4. Combination of Identifiers:
   Combining multiple identifiers (e.g. short SHA + author) can also be used to uniquely identify a change in a codebase.
