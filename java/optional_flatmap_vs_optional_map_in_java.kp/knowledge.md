---
title: How does optional.flatmap differ from optional.map?
authors:
- nanja_dev
tags:
- java
- knowledge
thumbnail: images/java.png
created_at: 2023-02-06 00:00:00
updated_at: 2023-02-06 00:00:00
tldr: Optional.flatMap combines an Optional with a mapping function that returns an Optional, whereas Optional.map applies a mapping function that returns a non-Optional value.
---

**Contents**

[TOC]

#### Optional.map
Optional.map applies the given mapping function to the value contained in the Optional object and returns an Optional object containing the result. It does not flatten the result, so the mapping function must return an Optional object.

#### Optional.flatMap
Optional.flatMap applies the given mapping function to the value contained in the Optional object and returns an Optional object containing the flattened result. It will flatten the result of the mapping function, so the mapping function can return any type.
