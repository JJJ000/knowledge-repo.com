---
title: Configuring django for MySQL usage
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: Install the MySQL connector and configure the database settings in Django settings.py.
---

**Contents**

[TOC]

## Installing MySQL and MySQL Connector for Python

The first step in setting up Django to use MySQL is to install MySQL and the MySQL Connector for Python. 

1. Download and install MySQL Community Server from the official website (https://dev.mysql.com/downloads/mysql/).
2. Download and install MySQL Connector for Python from the official website (https://dev.mysql.com/downloads/connector/python/).

## Creating a MySQL database 

After installing MySQL, create a new database for use with Django.

1. Open the MySQL Command Line Client or any other MySQL client that you prefer.
2. Create a new database using the following command: `CREATE DATABASE <database_name>;`
3. Verify that the database was successfully created by running the following command: `SHOW DATABASES;`

## Configuring Django to use MySQL

Now that MySQL and the MySQL Connector for Python are installed, and a new database has been created, you need to configure your Django project to use MySQL.

1. Open your Django project settings file (`settings.py`).
2. Under the `DATABASES` setting, set the `ENGINE` to `'django.db.backends.mysql'`.
3. Set the `NAME` of your database to the name that you created earlier.
4. Set the `USER` and `PASSWORD` to the credentials that you want to use to access the database.
5. Set the `HOST` and `PORT` if necessary.

```
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': '<database_name>',
        'USER': '<username>',
        'PASSWORD': '<password>',
        'HOST': '<database_hostname>',
        'PORT': '<database_port>',
    }
}
```

## Migrating your Django models to MySQL

Once your Django database is configured to use MySQL, you can migrate your existing Django models to MySQL.

1. Make sure your Django project has the necessary migration files by running `python manage.py makemigrations`.
2. Run `python manage.py migrate` to create the necessary tables in the MySQL database.
3. Verify that the migration was successful by running `SHOW TABLES;` in the MySQL client.
