---
title: What is the best way to set up a lazy onetoone relationship using jpa?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Use the @OneToOne annotation with the fetch parameter set to FetchType.LAZY.
---

**Contents**

[TOC]

1. Create a Lazy Fetch Type

The first step to creating a lazy OneToOne relation is to create a lazy fetch type. This can be done by adding the `@OneToOne` annotation to the field in the entity class and setting the `fetch` attribute to `FetchType.LAZY`.

Example:

```
@OneToOne(fetch = FetchType.LAZY)
private OtherEntity otherEntity;
```

2. Enable Proxying

In order to enable lazy loading of the relation, the JPA provider must be configured to enable proxying. This can be done by setting the `hibernate.enable_lazy_load_no_trans` property to `true`.

3. Set Lazy Loading Behavior

The JPA provider must also be configured to set the lazy loading behavior. This can be done by setting the `hibernate.default_lazy_load_no_trans` property to `true`.

4. Disable Fetch Joins

Finally, the JPA provider must also be configured to disable fetch joins. This can be done by setting the `hibernate.default_batch_fetch_size` property to `-1`. This will ensure that the related entity is not fetched when the parent entity is loaded.
