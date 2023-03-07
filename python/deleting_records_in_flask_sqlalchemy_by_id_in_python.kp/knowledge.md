---
title: What is the procedure for deleting a record based on its id in flask-sqlalchemy?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-03-07 00:00:00
updated_at: 2023-03-07 00:00:00
tldr: To delete a record by id in Flask-SQLAlchemy, use the following command Model.query.filter\_by(id=id).delete().
---

**Contents**

[TOC]

**Section 1: Introduction**

Flask-SQLAlchemy is a Flask extension that provides easy integration between Flask and SQLAlchemy, which is a popular and powerful database toolkit for Python. With Flask-SQLAlchemy, we can easily create, read, update and delete records in the database. In this tutorial, we will explore how to delete a record by id in Flask-SQLAlchemy.

**Section 2: Delete a record by id**

To delete a record by id in Flask-SQLAlchemy, we need to follow the below steps:

Step 1: Import the required modules

In order to use Flask-SQLAlchemy, we need to import the required modules. We need to import Flask class from the flask module, SQLAlchemy class from the flask_sqlalchemy module, and the app object that we created in our Flask application.

```python
from flask import Flask
from flask_sqlalchemy import SQLAlchemy

app = Flask(__name__)
app.config['SQLALCHEMY_DATABASE_URI'] = 'sqlite:///mydb.sqlite'
db = SQLAlchemy(app)
```

Step 2: Define the model

Next, we need to define the model for the table that we want to interact with. We can define the model using SQLAlchemy's class-based syntax. In this example, we will create a simple model for a user that has an id, name, and email.

```python
class User(db.Model):
    id = db.Column(db.Integer, primary_key=True)
    name = db.Column(db.String(50))
    email = db.Column(db.String(50))
```

Step 3: Delete the record

To delete the record, we need to first fetch the record using the id. Once we have the record, we can use the db.session.delete() method to delete the record.

```python
user = User.query.get(id)
if user:
    db.session.delete(user)
    db.session.commit()
```

The above code first fetches the record using the id, and then checks if the record exists. If the record exists, it then deletes the record using the db.session.delete() method and commits the changes using the db.session.commit() method.

Step 4: Complete Code

```python
from flask import Flask
from flask_sqlalchemy import SQLAlchemy

app = Flask(__name__)
app.config['SQLALCHEMY_DATABASE_URI'] = 'sqlite:///mydb.sqlite'
db = SQLAlchemy(app)

class User(db.Model):
    id = db.Column(db.Integer, primary_key=True)
    name = db.Column(db.String(50))
    email = db.Column(db.String(50))

@app.route('/delete_user/<int:id>', methods=['POST'])
def delete_user(id):
    user = User.query.get(id)
    if user:
        db.session.delete(user)
        db.session.commit()
        return 'User deleted successfully'
    else:
        return 'User not found'

if __name__ == '__main__':
    app.run()
```

The above code defines a Flask route `/delete_user/<int:id>` that accepts a POST request with an id parameter. It then fetches the record using the id, deletes the record using the db.session.delete() method, and commits the changes using the db.session.commit() method. Finally, it returns a success message if the record was deleted, or an error message if the record was not found.

**Section 3: Conclusion**

We successfully learned how to delete a record by id in Flask-SQLAlchemy. We also explored the steps involved in this process, which include importing the required modules, defining the model, deleting the record, and committing the changes. By following the above steps, you can easily delete records in your Flask-SQLAlchemy application.
