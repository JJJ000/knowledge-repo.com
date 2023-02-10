---
title: What is the process for implementing select2 with JSON data via an ajax request?
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-10 00:00:00
updated_at: 2023-02-10 00:00:00
tldr: Use the ajax option to specify an Ajax request to retrieve the JSON data for the Select2 dropdown.
---

**Contents**

[TOC]

1. Initializing Select2

In order to use Select2 with JSON via Ajax request, you must first initialize the Select2 widget. This can be done by selecting the element you wish to bind the Select2 widget to, and then calling the Select2 function on that element.

For example:

```javascript
$('#mySelect2Element').select2();
```

2. Configuring Ajax Request

Next, you must configure the Ajax request to use the JSON data. This is done by passing an object to the Select2 function with the `ajax` property set to an object containing the URL and dataType for the Ajax request.

For example:

```javascript
$('#mySelect2Element').select2({
  ajax: {
    url: 'https://example.com/data.json',
    dataType: 'json'
  }
});
```

3. Configuring Results

The next step is to configure how the results will be displayed. This is done by setting the `results` property of the `ajax` object to a function that takes the response from the Ajax request and returns the data to be displayed in the Select2 widget.

For example:

```javascript
$('#mySelect2Element').select2({
  ajax: {
    url: 'https://example.com/data.json',
    dataType: 'json',
    results: function(data) {
      return {
        results: data.items
      };
    }
  }
});
```

4. Configuring Search

Finally, you must configure how the search is performed. This is done by setting the `processResults` property of the `ajax` object to a function that takes the response from the Ajax request and returns the filtered data to be displayed in the Select2 widget.

For example:

```javascript
$('#mySelect2Element').select2({
  ajax: {
    url: 'https://example.com/data.json',
    dataType: 'json',
    results: function(data) {
      return {
        results: data.items
      };
    },
    processResults: function (data, params) {
      var filteredData = data.items.filter(function(item) {
        return item.name.toLowerCase().indexOf(params.term.toLowerCase()) > -1;
      });
      return {
        results: filteredData
      };
    }
  }
});
```
