---
title: What is the jquery code to launch a bootstrap modal?
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: Use the jQuery .modal() function to open a Bootstrap modal window.
---

**Contents**

[TOC]

## 1. Add the Modal HTML

The first step is to add the modal HTML to your web page. This HTML should contain the modal's content, as well as the modal's trigger button.

```html
<div class="modal fade" id="myModal">
  <div class="modal-dialog">
    <div class="modal-content">
      <div class="modal-header">
        <h4 class="modal-title">Modal Title</h4>
        <button type="button" class="close" data-dismiss="modal">&times;</button>
      </div>
      <div class="modal-body">
        Modal body text goes here.
      </div>
      <div class="modal-footer">
        <button type="button" class="btn btn-danger" data-dismiss="modal">Close</button>
      </div>
    </div>
  </div>
</div>

<button type="button" class="btn btn-primary" data-toggle="modal" data-target="#myModal">Open Modal</button>
```

## 2. Add the jQuery

The next step is to add the jQuery code to open the modal window. This code should be added to a `<script>` tag in the page.

```javascript
$(document).ready(function(){
  $("#myModal").modal();
});
```

## 3. Testing the Modal

Once the HTML and jQuery code is added to the page, the modal should be tested to ensure it is working properly. To do this, simply click the trigger button to open the modal.

## 4. Closing the Modal

The modal can be closed by clicking the close button or by clicking outside of the modal window.
