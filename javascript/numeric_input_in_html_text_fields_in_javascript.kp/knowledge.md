---
title: An html text input field only accepts numerical values
authors:
- smooth_flow
tags:
- javascript
- knowledge
thumbnail: images/javascript.png
created_at: 2023-02-03 00:00:00
updated_at: 2023-02-03 00:00:00
tldr: A text input can be restricted to accept only numeric input by using the `pattern` attribute with a regular expression to match desired input.
---

**Contents**

[TOC]

**Section 1: Creating the Input**

The first step to creating a text input that only allows numeric input is to create the text input itself. This can be done with HTML code, such as `<input type="text" id="myInput" />`. This will create a text input with the ID of "myInput".

**Section 2: Adding Javascript**

The next step is to add a bit of Javascript to the code. This code will check the value of the text input when it is changed, and only allow numbers to be entered. The code below will do this:

```
<script>
    document.getElementById('myInput').onchange = function() {
        if(isNaN(this.value)) {
            alert('Please enter a number!');
            this.value = '';
        }
    }
</script>
```

**Section 3: Testing the Input**

Once the code is added, the input can be tested to make sure it works as expected. If a non-numeric value is entered into the input, an alert should appear saying "Please enter a number!" and the value should be cleared.

**Section 4: Conclusion**

In conclusion, it is possible to create a text input that only allows numeric input by using HTML and Javascript. The code provided in this answer will do this, and can be tested to make sure it works as expected.
