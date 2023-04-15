---
title: Incorporating a user into a group using django
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: Use the `add()` method to add a user to a group in Django, like this `group.user\_set.add(user)`.
---

**Contents**

[TOC]

## Overview

In Django, adding a user to a group can be done using the `User.groups.add()` method or through the `Group.user_set.add()` method. The former approach involves accessing the groups attribute of the User model, while the latter involves accessing the user_set attribute of the Group model. 

This article will explain both approaches in more detail.

## Add a User to a Group using User.groups.add()

```python
from django.contrib.auth.models import User, Group

# Get the User and Group objects
user = User.objects.get(username='john')
group = Group.objects.get(name='admin')

# Add the user to the group
user.groups.add(group)
```

This approach involves accessing the `groups` attribute of the User model, which is a ManyToManyField to the Group model. To add the user to a group, simply call the `add()` method on the groups attribute of the user object, passing in the group object as an argument.

## Add a User to a Group using Group.user_set.add()

```python
from django.contrib.auth.models import User, Group

# Get the User and Group objects
user = User.objects.get(username='john')
group = Group.objects.get(name='admin')

# Add the user to the group
group.user_set.add(user)
```

This approach involves accessing the `user_set` attribute of the Group model, which is a ManyToManyField to the User model. To add the user to a group, simply call the `add()` method on the user_set attribute of the group object, passing in the user object as an argument.

## Conclusion

Both approaches achieve the same result of adding a user to a group in Django. The first approach is more convenient if you already have the user object and want to add it to a group, while the second approach is more convenient if you already have the group object and want to add a user to it.
