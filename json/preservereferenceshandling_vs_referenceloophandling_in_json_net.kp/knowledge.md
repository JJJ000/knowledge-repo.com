---
title: How do preservereferenceshandling and referenceloophandling differ in json.net?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-14 00:00:00
updated_at: 2023-02-14 00:00:00
tldr: PreserveReferencesHandling determines how object references are preserved when serializing and deserializing, while ReferenceLoopHandling determines how to handle self-referencing objects when serializing and deserializing.
---

**Contents**

[TOC]

# PreserveReferencesHandling
PreserveReferencesHandling determines how object references are preserved when serializing and deserializing objects. When serializing an object, PreserveReferencesHandling will preserve any object references that are encountered. When deserializing an object, PreserveReferencesHandling will use the object references that were preserved during serialization. This can be useful when dealing with circular references.

# ReferenceLoopHandling
ReferenceLoopHandling determines how object references are handled when serializing and deserializing objects. When serializing an object, ReferenceLoopHandling will ignore any object references that are encountered. When deserializing an object, ReferenceLoopHandling will throw an exception if it encounters an object reference that it cannot resolve. This can be useful when dealing with circular references.
