---
title: What is the process for running raw sql queries in a flask-sqlalchemy application?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-05 00:00:00
updated_at: 2023-02-05 00:00:00
tldr: Use the db.engine.execute() method to execute raw SQL in a Flask-SQLAlchemy app.
---

**Contents**

[TOC]

# Section 1: Setting up

In order to execute raw SQL in Flask-SQLAlchemy, you must first set up your Flask-SQLAlchemy app. This involves creating a Flask app, connecting to a database, and creating a SQLAlchemy object.

# Section 2: Creating a Session

Once you have a Flask-SQLAlchemy app set up, you must then create a session. This session will allow you to execute raw SQL queries.

# Section 3: Executing Raw SQL Queries

Once you have a session created, you can then execute raw SQL queries. To execute a query, you must use the session.execute() method. This method takes a string argument which is the raw SQL query you want to execute.

# Section 4: Closing the Session

Finally, once you have finished executing your raw SQL queries, you must close the session. To do this, you must use the session.close() method. This will close the session and free up any resources that were used during the session.
