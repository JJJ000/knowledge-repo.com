---
title: What is the difference between jpa joincolumn and mappedby?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: JoinColumn is used to define the foreign key column of the table, while mappedBy is used to define the inverse side of the relationship.
---

**Contents**

[TOC]

1. **JoinColumn**
- JoinColumn is used to define a foreign key column in the table of the owning entity. It is used when the relationship is unidirectional, i.e. when the target entity does not have a reference back to the source entity. It is used when the relationship between two entities is one-to-one or one-to-many.

2. **MappedBy**
- MappedBy is used to define the entity that owns the relationship. It is used when the relationship is bidirectional, i.e. when the target entity has a reference back to the source entity. It is used when the relationship between two entities is many-to-one or many-to-many.
