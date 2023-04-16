---
title: Using jquery to set the chosen value of a select control based on its text description
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-04-15 00:00:00
updated_at: 2023-04-15 00:00:00
tldr: jQuery`s `val()` function can be used to set the selected value of a select control by passing in the text description of the desired option.
---

**Contents**

[TOC]

1. Retrieve the Value of the Select Option 

Using jQuery, you can retrieve the value of the select option by using the `val()` method. This method will return the value of the first selected option in the select list. 

```
var selectedValue = $("#mySelect").val();
```

2. Set the Selected Value of the Select Option 

Using jQuery, you can set the selected value of the select option by using the `val()` method. This method will set the value of the first selected option in the select list. 

```
$("#mySelect").val("myValue");
```

3. Retrieve the Text of the Select Option

Using jQuery, you can retrieve the text of the select option by using the `text()` method. This method will return the text of the first selected option in the select list. 

```
var selectedText = $("#mySelect option:selected").text();
```

4. Set the Selected Value of the Select Option via Text

Using jQuery, you can set the selected value of the select option by using the `filter()` and `val()` methods. This method will set the value of the option in the select list that has the text description that matches the provided text. 

```
$("#mySelect").filter(function(){
    return $(this).text() == 'myText';
}).val();
```
