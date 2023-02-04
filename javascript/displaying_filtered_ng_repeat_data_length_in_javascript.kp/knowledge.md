---
title: What is the length of the data returned by the filtered ng-repeat?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-04 00:00:00
updated_at: 2023-02-04 00:00:00
tldr: The length of the filtered ng-repeat data can be displayed using the `length` property of the filtered array.
---

**Contents**

[TOC]

# Section 1: Filtering the Data

Using AngularJS, you can filter an ng-repeat expression using a custom filter. For example, if you had a list of items, you could filter the list based on a certain criteria. To do this, you would use the `filter` option in the ng-repeat expression.

For example:

```
<div ng-repeat="item in items | filter:criteria">
  {{item}}
</div>
```

In the above example, the ng-repeat expression will filter the items list based on the criteria specified.

# Section 2: Calculating the Length

Once you have filtered the data, you can then calculate the length of the filtered data using the `length` property. For example, if you had a filtered list of items, you could calculate the length of the list using the following code:

```
var length = filteredItems.length;
```

# Section 3: Displaying the Length

Once you have calculated the length of the filtered data, you can then display the length on the page. To do this, you can use the `{{length}}` expression in the HTML. For example:

```
<p>The length of the filtered list is {{length}}.</p>
```

# Section 4: Updating the Length

Finally, you can also update the length of the filtered data when the filter criteria is changed. To do this, you can use the `$watch` method in AngularJS. This will watch the filter criteria for changes and update the length of the filtered data accordingly. For example:

```
$scope.$watch('criteria', function() {
  $scope.length = filteredItems.length;
});
```
