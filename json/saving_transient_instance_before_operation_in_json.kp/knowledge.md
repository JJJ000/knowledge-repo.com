---
title: A not-null property is referencing a transient value, so the transient instance must be saved before proceeding with the current operation
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-18 00:00:00
updated_at: 2023-02-18 00:00:00
tldr: The transient instance must be saved before the current operation can be completed.
---

**Contents**

[TOC]

1. What is a Transient Value?

A transient value is an object or variable that is not stored in the database and is not accessible outside the scope of the current operation. It is used to temporarily store data and is usually discarded once the operation is complete.

2. What is a Not-null Property?

A not-null property is an attribute in a database table that cannot contain a null value. It is used to ensure that a value is present in the database and is usually used to enforce data integrity.

3. What is the Relationship Between Transient Values and Not-null Properties?

When a transient value is referenced in a not-null property, the transient value must be saved before the current operation in JSON. This is because the not-null property requires a value that is stored in the database, not a transient value.

4. How to Save a Transient Value?

A transient value can be saved by using the appropriate methods of the object-relational mapping (ORM) framework that is being used. For example, in Hibernate, the save() or persist() method can be used to save a transient value in the database.
