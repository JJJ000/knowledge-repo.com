---
title: Updating database with sqlalchemy orm in an effective manner
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-13 00:00:00
updated_at: 2023-03-13 00:00:00
tldr: Use the `session.commit()` method to efficiently update a database using SQLAlchemy ORM in Python.
---

**Contents**

[TOC]

Advantages of SQLAlchemy ORM for database updates

1. Simplified syntax: SQLAlchemy ORM provides a simplified syntax for database operations, allowing developers to interact with the database using Python classes and objects rather than raw SQL queries.

2. Protection from SQL injection attacks: ORM libraries like SQLAlchemy have built-in protection against SQL injection attacks, making it significantly easier and safer to update databases.

3. Cross-platform compatibility: Since SQLAlchemy is a cross-platform library, it can be used with various SQL databases such as PostgreSQL, MySQL, Oracle and SQLite, making it easy to update databases across an organization in a standardized way.

4. Increased code readability: SQLAlchemy ORM provides more concise and expressive code compared to traditional SQL queries, making it easier to understand and maintain code for database updates.

Updating a database using SQLAlchemy ORM

Here are the steps to efficiently update a database using the SQLAlchemy ORM:

1. Creating a database session: To update the database using SQLAlchemy ORM, we first need to create a database session. The session enables us to interact with the database using objects and classes instead of raw SQL queries.

```
from sqlalchemy.orm import sessionmaker
from models import engine, User

Session = sessionmaker(bind=engine)
session = Session()
```

2. Retrieving data from the database: To update the data in the database, we first need to retrieve the existing data using an appropriate query.

```
user = session.query(User).filter(User.id == 1).first()
```

3. Updating the data: SQLAlchemy ORM provides a simple way to update the data in the database using the object attributes.

```
user.name = "John Doe"
user.email = "johndoe@example.com"
session.add(user)
session.commit()
```

4. Closing the session: Once we have updated the data in the database, we need to close the session to avoid any resource leaks.

```
session.close()
```

Efficient tips for database updates using SQLAlchemy ORM

1. Use bulk updates: To improve the efficiency of database updates when working with large datasets, we can use bulk updates. SQLAlchemy ORM provides a method called `update` which can update multiple rows in the database in a single transaction.

```
session.query(User).filter(User.id.in_([1, 2, 3])).update({User.active: True})
```

2. Use batch commit: If we are updating a large number of rows in the database, it's a good practice to use batch commit. Batch commit provides a way to commit transactions in batches to avoid memory overflow caused by large transactions.

```
from sqlalchemy import event

@event.listens_for(session, 'before_flush')
def batch_flush(session, flush_context, instances):
    session.commit()
```

3. Optimize queries: We can also optimize the queries by selecting only the columns we need instead of loading the whole row. This reduces the amount of data transferred from the database to the application and improves the performance of the database updates.

```
users = session.query(User.name, User.email).all()
```

4. Use indexes: Indexes can significantly improve the performance of database updates by reducing the amount of time the database takes to search for the rows to update. Therefore, it is advisable to create indexes on the columns that are frequently updated.

```
from sqlalchemy import Index

Index('index_user_email', User.email)
```
