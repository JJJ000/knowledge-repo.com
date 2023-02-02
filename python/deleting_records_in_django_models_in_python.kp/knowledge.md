---
title: What is the process for removing a record from a django model?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-02-02 00:00:00
updated_at: 2023-02-02 00:00:00
tldr: To delete a record in Django models, use the .delete() method.
---

**Contents**

[TOC]

# Section 1: Locate the Record

To delete a record in Django models, first locate the record you wish to delete. You can locate the record using the Django ORM (Object-Relational Mapping) query methods.

# Section 2: Delete the Record

Once you have located the record, you can delete it using the delete() method. This method will delete the record from the database.

# Section 3: Save the Changes

After deleting the record, you must save the changes. This can be done by calling the save() method on the object.

# Section 4: Refresh the Page

Finally, you must refresh the page to see the changes. This can be done by refreshing the page in the browser or by using the refresh_from_db() method.
