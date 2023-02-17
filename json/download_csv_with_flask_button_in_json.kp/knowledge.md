---
title: Download a csv file from flask by clicking a button
authors:
- cool_wizard
tags:
- json
- knowledge
thumbnail: images/json.png
created_at: 2023-02-17 00:00:00
updated_at: 2023-02-17 00:00:00
tldr: Yes, it is possible to download a csv file on clicking a button in JSON using Flask.
---

**Contents**

[TOC]

**Section 1: Create the Flask Application**

To download a csv file on clicking a button in a JSON response, the first step is to create a Flask application. Flask is a Python web framework used for developing web applications. To create a Flask application, you need to first import the Flask module and then create an instance of the Flask class. The following code snippet shows an example of a Flask application:

```python
from flask import Flask

app = Flask(__name__)

@app.route('/')
def index():
   return 'Hello World!'

if __name__ == '__main__':
   app.run()
```

**Section 2: Create the JSON Response**

Once the Flask application has been created, the next step is to create the JSON response that will contain the button that will be used to trigger the download of the csv file. The JSON response can be created using the jsonify() method of the Flask module. The following code snippet shows an example of a JSON response containing a button:

```python
from flask import jsonify

@app.route('/download_csv')
def download_csv():
   data = {
      'button': '<button type="button" onclick="downloadCSV()">Download CSV</button>'
   }
   return jsonify(data)
```

**Section 3: Create the Download Function**

The next step is to create the download function that will be triggered when the button in the JSON response is clicked. The download function can be created using the send_file() method of the Flask module. The send_file() method takes a file path as an argument and sends the file to the client. The following code snippet shows an example of a download function:

```python
from flask import send_file

@app.route('/download_csv')
def download_csv():
   try:
      return send_file('data.csv',
                       attachment_filename='data.csv',
                       as_attachment=True)
   except Exception as e:
      return str(e)
```

**Section 4: Add JavaScript to Trigger the Download**

The last step is to add JavaScript code to the JSON response that will trigger the download function when the button is clicked. The JavaScript code can be added using the script tag in the JSON response. The following code snippet shows an example of a JavaScript code that will trigger the download function:

```javascript
<script>
   function downloadCSV() {
      fetch('/download_csv')
         .then(response => {
            if (response.ok) {
               response.blob().then(blob => {
                  let url = window.URL.createObjectURL(blob);
                  let a = document.createElement('a');
                  a.href = url;
                  a.download = 'data.csv';
                  a.click();
               });
            }
         });
   }
</script>
```
