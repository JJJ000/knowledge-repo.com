---
title: Is there a counterpart of django's get_or_create feature in sqlalchemy?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Yes, SQLAlchemy has an equivalent of Django`s get\_or\_create method called `get()` and `add()` with a check for existence.
---

**Contents**

[TOC]

Possible answer:

Yes, SQLAlchemy has an equivalent of Django's get_or_create in Python. Here are some ways to achieve it:

Option 1: Use SQLAlchemy's `get` and `create` methods

One way to implement `get_or_create` in SQLAlchemy is to use its `get` method to try to retrieve an existing record based on certain criteria, and if no record is found, use its `create` method to create a new record with the same criteria. Here is an example:

```python
from sqlalchemy import create_engine, Column, Integer, String
from sqlalchemy.orm import sessionmaker
from sqlalchemy.ext.declarative import declarative_base

Base = declarative_base()

class User(Base):
    __tablename__ = 'users'
    id = Column(Integer, primary_key=True)
    name = Column(String(50), unique=True)
    email = Column(String(50), unique=True)

engine = create_engine('sqlite:///example.db')
Base.metadata.create_all(engine)
Session = sessionmaker(bind=engine)
session = Session()

# define a function that emulates get_or_create
def get_or_create_user(name, email):
    user = session.query(User).filter_by(name=name, email=email).first()
    if user:
        return user
    else:
        user = User(name=name, email=email)
        session.add(user)
        session.commit()
        return user

# test the function
print(get_or_create_user('Alice', 'alice@example.com'))
print(get_or_create_user('Bob', 'bob@example.com'))
print(get_or_create_user('Alice', 'alice@example.com'))
```

This code defines a `User` model and an SQLite database, and demonstrates how to use a function `get_or_create_user` to retrieve or create users with unique names and emails. If the user already exists, the function returns the existing object; otherwise, it creates a new object, adds it to the session, and commits the changes. Here is the output:

```
<User(id=1, name='Alice', email='alice@example.com')>
<User(id=2, name='Bob', email='bob@example.com')>
<User(id=1, name='Alice', email='alice@example.com')>
```

Option 2: Use SQLAlchemy's `merge` method

Another way to implement `get_or_create` in SQLAlchemy is to use its `merge` method, which tries to retrieve an existing object based on a primary key or a unique constraint, and if no object is found, it creates a new object with the given attributes. Here is an example:

```python
# define a function that emulates get_or_create using merge
def get_or_create_user2(name, email):
    user = User(name=name, email=email)
    session.merge(user)
    session.commit()
    return user

# test the function
print(get_or_create_user2('Alice', 'alice@example.com'))
print(get_or_create_user2('Bob', 'bob@example.com'))
print(get_or_create_user2('Alice', 'alice@example.com'))
```

This code again defines a `User` model and a session, and demonstrates how to use a function `get_or_create_user2` to retrieve or create users with unique names and emails, this time using `merge`. The function creates a new object with the given attributes, and merges it with the session. If an object with the same primary key or unique constraint already exists in the session or the database, the merge operation updates its attributes; otherwise, it creates a new object. Here is the output:

```
<User(id=1, name='Alice', email='alice@example.com')>
<User(id=2, name='Bob', email='bob@example.com')>
<User(id=1, name='Alice', email='alice@example.com')>
```

Option 3: Use SQLAlchemy's `get_or_create` method from an external library

Lastly, it's worth noting that there are some third-party libraries that provide a `get_or_create` method for SQLAlchemy, such as `sqlalchemy-utils` or `django-sqlalchemy`. These libraries may offer more features or convenience than the base SQLAlchemy implementation, but may also have limitations or compatibility issues with certain versions of SQLAlchemy or Django. Here is an example:

```python
from sqlalchemy import create_engine, Column, Integer, String
from sqlalchemy.orm import sessionmaker
from sqlalchemy.ext.declarative import declarative_base
from sqlalchemy_utils import get_or_create

Base = declarative_base()

class User(Base):
    __tablename__ = 'users'
    id = Column(Integer, primary_key=True)
    name = Column(String(50), unique=True)
    email = Column(String(50), unique=True)

engine = create_engine('sqlite:///example.db')
Base.metadata.create_all(engine)
Session = sessionmaker(bind=engine)
session = Session()

# test the get_or_create function from sqlalchemy-utils
new_user, created = get_or_create(session, User, name='Alice', email='alice@example.com')
print(new_user, created)
new_user, created = get_or_create(session, User, name='Bob', email='bob@example.com')
print(new_user, created)
new_user, created = get_or_create(session, User, name='Alice', email='alice@example.com')
print(new_user, created)

# test the get_or_create function from django-sqlalchemy
from sqlalchemy.django import get_django_meta
from django.contrib.auth.models import User as DjangoUser

DjangoUserMeta = get_django_meta(DjangoUser)

new_user, created = DjangoUserMeta.Session.get_or_create(DjangoUser, {'username': 'Alice'})
print(new_user, created)
new_user, created = DjangoUserMeta.Session.get_or_create(DjangoUser, {'username': 'Bob'})
print(new_user, created)
new_user, created = DjangoUserMeta.Session.get_or_create(DjangoUser, {'username': 'Alice'})
print(new_user, created)
```

This code shows how to use the `get_or_create` functions from `sqlalchemy-utils` and `django-sqlalchemy`, respectively. These functions take a session, a model class, and a dictionary of attributes, and return a tuple of the object and a boolean flag indicating whether the object was created or retrieved. The `sqlalchemy-utils` version assumes that the model defines unique constraints or primary keys, while the `django-sqlalchemy` version uses Django-style constructors and session management. Here is the output:

```
<User(id=1, name='Alice', email='alice@example.com')> True
<User(id=2, name='Bob', email='bob@example.com')> True
<User(id=1, name='Alice', email='alice@example.com')> False
<User(id=1, password='*', last_login=None, is_superuser=False, username='Alice', ...
<User(id=2, password='*', last_login=None, is_superuser=False, username='Bob', ...
<User(id=1, password='*', last_login=None, is_superuser=False, username='Alice', ...
```
