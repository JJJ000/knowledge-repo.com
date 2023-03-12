---
title: Django encounters a "mysql error of incorrect string value" while attempting to store a unicode string in its database
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-12 00:00:00
updated_at: 2023-03-12 00:00:00
tldr: The issue can be resolved by ensuring that the database and tables are properly configured to support UTF-8 encoding.
---

**Contents**

[TOC]

## Introduction

MySQL is a popular open-source relational database management system used in web applications. Django, a high-level Python web framework, is commonly used with MySQL to create robust and scalable web applications. Sometimes, MySQL may throw an "incorrect string value" error when attempting to save a Unicode string in Django.

## Causes of "incorrect string value" error

There are two common causes of the "incorrect string value" error when attempting to save a Unicode string in Django:

1. The database or table does not have the correct character set encoding to support Unicode.
2. The connection between Django and MySQL is not using UTF-8 character set encoding.

## Solutions for "incorrect string value" error

### Solution 1: Change the database or table character set encoding

One solution to the "incorrect string value" error is to change the character set encoding of the database or table to UTF-8. This will allow the database to properly store and retrieve Unicode strings. To change the encoding, follow these steps:

1. Login to MySQL as a user with administrative privileges.
2. Use the `ALTER DATABASE` or `ALTER TABLE` command to change the character set encoding to UTF-8:

```sql
ALTER DATABASE mydatabase CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
```

```sql
ALTER TABLE mytable CONVERT TO CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
```

### Solution 2: Change the connection character set encoding in Django settings

Another solution to the "incorrect string value" error is to ensure that Django is connecting to MySQL using UTF-8 character set encoding. To do this, add the following lines to the Django `settings.py` file:

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'mydatabase',
        'USER': 'mydatabaseuser',
        'PASSWORD': 'mydatabasepassword',
        'HOST': 'localhost',
        'PORT': '',
        'OPTIONS': {
            'charset': 'utf8mb4',
        },
    }
}
```

This will ensure that Django is connecting to MySQL using UTF-8 character set encoding.

## Conclusion

The "incorrect string value" error when attempting to save a Unicode string in Django can be caused by a mismatch in character set encoding between the database, table, and Django. By changing the character set encoding of the database or table to UTF-8, or by ensuring that Django is connecting to MySQL using UTF-8 character set encoding, the error can be resolved.
