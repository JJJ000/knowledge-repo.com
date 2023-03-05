---
title: Changes made to the JSON field are not saved in the database
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-03-05 00:00:00
updated_at: 2023-03-05 00:00:00
tldr: Json fields are immutable in PostgreSQL, so updates to JSON fields require creating a new record rather than modifying an existing one.
---

**Contents**

[TOC]

## Possible reasons:

### Cache
If there is a cache involved in the application, a common reason for updates not persisting to the database is that the values in the cache are not updated properly. This may lead to the application not reading the updated values from the database and instead serving up the old cached values.

### Incorrect Model Setup
Another reason for updates not persisting to the database is an incorrect model setup that does not properly handle JSON fields. This could include missing or incorrect field definitions, incorrect mappings, or incorrect serialization/deserialization settings.

### Database Configuration
It's also possible that updates are not persisting because of an underlying issue with the database itself. This could include incorrect database configuration, missing or improperly set up database indexes, or issues with the database engine.

### Security and Permissions
Finally, another possible issue could be related to security and permissions. If the user does not have the proper permissions to update the JSON fields in the database, the update will fail and the changes will not be persisted. 

## Troubleshooting steps:

- Check the cache implementation and make sure it is properly configured to update values when changes are made to the database.
- Review the model setup and ensure that the JSON fields are properly defined and mapped. Check the serialization/deserialization settings as well.
- Review the database logs and look for any errors related to the failed updates. Consider checking database indexes and engine configuration.
- Review the application's security and permission settings to ensure that the user has the proper permissions to update JSON fields in the database.
