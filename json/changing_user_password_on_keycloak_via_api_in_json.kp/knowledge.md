---
title: What is the procedure for altering a user's password in keycloak using an API call?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-16 00:00:00
updated_at: 2023-02-16 00:00:00
tldr: Yes, the Keycloak Admin REST API includes an endpoint for resetting user passwords.
---

**Contents**

[TOC]

## Overview

Keycloak is an open source identity and access management solution. It provides a single sign-on solution for web applications, mobile applications, and RESTful web services. It also provides an API for managing user accounts, including the ability to change user passwords.

## API Call

The API call for changing a user password in Keycloak is `PUT /{realm}/users/{id}/reset-password`. This API call requires the user ID and the new password.

## Parameters

The parameters for the `PUT /{realm}/users/{id}/reset-password` API call are as follows:

- `realm`: The name of the realm in which the user is registered.
- `id`: The ID of the user.
- `password`: The new password for the user.

## JSON Format

The JSON format for the `PUT /{realm}/users/{id}/reset-password` API call is as follows:

```json
{
    "realm": "<realm_name>",
    "id": "<user_id>",
    "password": "<new_password>"
}
```
