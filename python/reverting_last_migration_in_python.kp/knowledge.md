---
title: What is the process for undoing the most recent migration?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: To revert the last migration in Python, use the `migrate` command with the `--reverse-code` flag.
---

**Contents**

[TOC]

# Section 1: Check Your Migration Status

Before you can revert a migration, you'll need to check the current migration status of your Python project. This can be done by running the `showmigrations` command. This will show you all the migrations that have been applied to your project, and the status of each one.

# Section 2: Revert the Last Migration

Once you know the status of your migrations, you can then use the `migrate --backward` command to revert the last migration. This command will take the last migration that was applied to your project and revert it to its previous state.

# Section 3: Check Your Migration Status Again

Once you have reverted the last migration, you should check the migration status again to make sure it has been applied correctly. Run the `showmigrations` command again to see the updated status of your migrations.

# Section 4: Apply the Reverted Migration

Once you have confirmed the reverted migration has been applied correctly, you can then apply it again with the `migrate` command. This will apply the reverted migration to your project, and you should now be back to the state you were in before the last migration was applied.
