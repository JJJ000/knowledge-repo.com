---
title: What is the distinction between the role and grantedauthority objects in spring security?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: A Role is a logical grouping of GrantedAuthority objects that represent a user`s permissions.
---

**Contents**

[TOC]

### Role

A role is a set of permissions that can be assigned to a user. It is usually used to define a user's access level. Roles are used to define the user's ability to access certain resources or perform certain actions.

### GrantedAuthority

GrantedAuthority is an interface in the Spring Security framework. It is used to represent a user's roles and permissions. It is used to define a user's access level and the resources or actions they can access. It is used to secure resources and define user roles.
