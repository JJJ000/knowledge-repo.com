---
title: Having various modeladmins/views for a single model in django's administrative interface
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-08 00:00:00
updated_at: 2023-03-08 00:00:00
tldr: Yes, multiple ModelAdmins/views can be defined for the same model in Django admin by subclassing the original ModelAdmin and customizing it according to requirements.
---

**Contents**

[TOC]

Section 1: Introduction
Django admin is powerful built-in web-based graphical interface provided by Django for developers to manage their application data. However, there are situations where a single model can have multiple models admins/views for it. In this article, we will explain how to implement multiple model-admins/views for the same model in Django admin.

Section 2: Model Inheritance
One approach is to use model inheritance to create multiple model admins/views for the same model. To achieve this, the base model will serve as the parent class, and the new model would inherit its attribute and methods. Then, we would create another ModelAdmin class for the new model to populate the specific attributes and their methods.

Section 3: Custom ModelAdmin
Another approach would be to subclass Django's built-in ModelAdmin and add custom attributes and methods to it. Then, we can register multiple instances of the ModelAdmin subclass for the same model with different names. This way, we can have multiple model admins/views for the same model with distinct functionalities.

Section 4: Proxy Model
Finally, we can use proxy models to achieve multiple ModelAdmins/views for the same model. By default, Django will create a new database table for every model in Django. However, when we create a proxy model for the same model, Django will use the same database table as the original model, but with a different ModelAdmin/view that we can customize separately. 

Conclusion
In summary, there are different approaches that we can utilize to create multiple model admins/views for the same model to provide distinct functionalities for our Django application. Developers can choose whichever approach suits their needs best to optimize management of their application data.
