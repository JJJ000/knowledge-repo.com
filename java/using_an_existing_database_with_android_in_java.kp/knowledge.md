---
title: What steps are needed to connect an Android application to an existing database?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-01-29 00:00:00
updated_at: 2023-01-29 00:00:00
tldr: To use an existing database with an Android application in Java, you must use the Room Persistence Library to map the database to Java objects.
---

**Contents**

[TOC]

### Setup

1. Create a new Android project in Android Studio.
2. Add the necessary dependencies to your project's `build.gradle` file.
3. Create a `DatabaseHelper` class to interact with the database.
4. Add the existing database file to the `assets` folder of your Android project.

### Database Access

1. Open the database using the `SQLiteDatabase` class.
2. Create a `Cursor` object to access the data in the database.
3. Use the `Cursor` object to read and write data to the database.

### Queries

1. Create `SELECT`, `INSERT`, `UPDATE` and `DELETE` queries to access and modify the data in the database.
2. Use the `SQLiteDatabase` class to execute the queries.

### Error Handling

1. Handle any exceptions thrown when accessing the database.
2. Log any errors for debugging purposes.
