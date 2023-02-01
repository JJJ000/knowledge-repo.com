---
title: What is the distinction between the flush() and commit() functions in sqlalchemy?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-01 00:00:00
updated_at: 2023-02-01 00:00:00
tldr: Flush() will write all the pending changes to the database, but won`t commit them, while commit() will write the pending changes to the database and commit them.
---

**Contents**

[TOC]

#### Flush
Flush is an operation used to synchronize the state of objects with the database. It updates the database with the changes made to the objects in the session. It also retrieves any newly generated primary keys and values of the columns that have server-side default values.

#### Commit
Commit is an operation used to save the changes made to the objects in the session to the database. It is a transaction control statement which makes all the changes made in the session permanent in the database. It also releases any locks held by the transaction.
