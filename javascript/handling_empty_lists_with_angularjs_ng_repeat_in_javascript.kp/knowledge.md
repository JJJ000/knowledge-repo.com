---
title: How does angularjs handle an empty list when using ng-repeat?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-07 00:00:00
updated_at: 2023-02-07 00:00:00
tldr: If the list is empty, ng-repeat will not render any elements.
---

**Contents**

[TOC]

**Section 1: ng-repeat Directive**

The AngularJS ng-repeat directive is used to iterate over a collection of items in the DOM. It is a powerful tool for creating dynamic views in AngularJS applications. It can be used to create lists, tables, and other collections of objects.

**Section 2: Handling Empty Lists**

When using the ng-repeat directive, it is important to handle empty lists. This can be done by using the “ng-if” directive to check if the list is empty. If the list is empty, the ng-if directive will display a message or other content to indicate that the list is empty.

**Section 3: Example Code**

Below is an example of how to use the ng-if directive to handle empty lists:

```
<div ng-if="!list || list.length === 0">
    <p>The list is empty.</p>
</div>

<div ng-repeat="item in list">
    <p>{{item}}</p>
</div>
```

**Section 4: Conclusion**

In conclusion, the ng-repeat directive is a powerful tool for creating dynamic views in AngularJS applications. When using the ng-repeat directive, it is important to handle empty lists by using the “ng-if” directive to check if the list is empty. If the list is empty, the ng-if directive will display a message or other content to indicate that the list is empty.
