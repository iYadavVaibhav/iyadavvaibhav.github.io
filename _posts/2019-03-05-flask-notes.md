---
title: Flask - WebFramework in Python 
layout: post
categories: notes python
last_modified_at: 2020-07-14 11:19:55
---

Flask is a microframework in Python. It is used to create a webapp. It can start a python web server. It can handle HTTP requests. It can also be used to make a webapp API.

* Do not remove this line (it will not be displayed)
{:toc}

## Virtual Environments

Why? - It gives different apps isolation and personal environment so that modules don't interfere and it is easy when we have to productionize the app.

What is Python Virtual Environment?  
- They are isolated environments where you can install packages as required.
- This creates a folder which contains all the necessary **executables** to use the packages that a Python project would need

How to use Virtual Environments in Python3?
- `python3 -m venv venv_app` - created folder venv_app
- `source venv_app/bin/activate` - activates this environment, for use
- now do `pip3 install flask` - this installs the package only in this environment.
- add `#!venv_app/bin/python3` on top of main.py file to make it use this python.

## Creating a Simple Flask App
We can start with the 'Hello World!' of flask app.

Create a python file:

```py
#!venv_app/bin/python3
from flask import Flask
app = Flask(__name__)

@app.route('/')
def index():
    return "Hello from Flask App!"

if __name__ == '__main__':
    app.run(debug=True)
```

## Running a flask app:
- `chmod a+x main.py ` to make app executable.
- `./main.py` runs app on localhost in debug mode.
- to access type `http://localhost:5000` in browser.

Access flask app on Virtual Machine localhost from host machine:
- Run flask app with `app.run(host='0.0.0.0', debug=True)`
- This tells your operating system to listen on all public IPs.
- then access `192.168.10.33:5000` from host machine.

Now that our app is running we can add a database to this app. We will use FlaskSQLAlchemy package for this.

## Flask-SQLAlchemy
It is an extension of `SQLAlchemy` which is ORM for major databases.
- It is an designe for Flask that adds support for SQLAlchemy to your application. 
- You can define table as a class, called model, with member variables as column names.
- Create an object to make new instance.
- Example

```py
class User(db.Model):
    __tablename__ = 'users'
    id = db.Column(db.Integer, primary_key = True)
    username = db.Column(db.String(50), unique=True)
    admin = db.Column(db.Boolean)
    created_on = db.Column(db.DateTime(), default=datetime.now)

db.session.add(obj)     # insert new record to database
db.session.delete(obj)  # delete a record from database
db.session.commit()     # updates modifications in object if any

# where clause
user = User.query.filter_by(username=data['username']).first() # or .all()

# select * from users
users = User.query.all()
```

Caution: 
- Provide full path to db file, so that apache can locate it.

## REST API and RESTful Web Services - The Basics Guide

What is REST?
- Client and Server are separate
- **Stateless:** No information from a request is stored on client to be used in other requests, eg, no session can be started, if authentication is required, username and password need to be sent with every request.

What is RESTful API:
- There is a resource, eg, tasks
- It has endpoints for CRUD operations
- HTTP methods, GET PUT POST DELETE, are used for these operations.
- Data is provided with these requests in no particular format but usually as:
  - JSON blob in request body, or
  - Query String arguments as portion of URL.


HTTP Method | URI | Action
-|-|-
GET | http://[hostname]/todo/api/v1.0/tasks | Retrieve list of tasks
GET | http://[hostname]/todo/api/v1.0/tasks/[task_id]| Retrieve a task
POST |  http://[hostname]/todo/api/v1.0/tasks | Create a new task
PUT | http://[hostname]/todo/api/v1.0/tasks/[task_id] | Update an existing task
DELETE |  http://[hostname]/todo/api/v1.0/tasks/[task_id] | Delete a task

Data of a task can be, JSON blob, as:

```py
{
  'id': 1,
  'title': 'Title of a to do task',
  'description': 'Description of to do task', 
  'done': False
}
```

- This API can be consumed by client side app which can be single page HTML.

---

# Flask Mega Tutorial Notes

In this tutorial by Miguel Grinberg, we are learning to crate a micro-blogging site using flask and other dependencies.

- `before_request` is a flask native function that gets executed before any request is made. It can be used to update last_seen timestamp.

## Create and Run Virtual Environment

- `python venv venv` creates a virtual environment with a dir 'venv' in root folder that has all python packages.
- Use `source venv/bin/activate` to activate it.

## Flask Debugging

- `export FLASK_DEBUG=0` makes the environment PROD else it is DEV or TEST.
- `export FLASK_APP=microblog.py` will make an variable that tells python which app to run.
- `flask run` executes the app or if flask is not in path then do `> python -m flask run`

## Flask DB Migrate commands
We can use to create table and manage changes
- `flask db init` creates migration folder 
- `flask db migrate` creates scripts for table creation
- `flask db upgrade` executes scripts to make table changes

## Start a python email server

`(venv) $ python -m smtpd -n -c DebuggingServer localhost:8025` this command starts emulated email server.

Some variables that we might need to export:
```
export MAIL_SERVER=smtp.googlemail.com
export MAIL_PORT=587
export MAIL_USE_TLS=1
export MAIL_USERNAME=email_id@domain.com
export MAIL_PASSWORD="password"
```

## Making new forms in app
We need to define following:
- **(M)** Form Class - in module `forms.py` make class with fields and validate functions.
- **(V)** HTML template - in `templates` folder, rendered from route with form passed as data. Display form elements, errors and hidden_tag.
- **(C)** Route - in module `routes.py`, define new route, import form class and use. On submit, create object of model class to save/query data.
- Create a link to access new route.

## Saving form data and tables
- **ORM** can be created in `modules.py`. We can define classes for our tables. Classes also define relationships. Have functions to query data.
- use them in routes to save and query data.
- uses db service to handle database operations.

## Routes.py
- imports forms classes from `forms.py` for:
    1. getting form data via POST
    2. passing form to html template for making form components and displaying errors

- import orm model classes from `models.py` for:
    1. making object of DB Table model
    2. submit and commit new data
    3. query model class to fetch data

## app \_\_init\_\_.py
This defines app folder as a python package. 
- It is where we link all modules (.py files in folder app) together as a Flask app.
- We import routes, models and error modules here.

**Services:** Here we have various services defined. We use them across app like db, login, mail.

## Blueprints
We can separate out application logical modules in application. Like we can create separate package for auth, error handling etc.

`from flask import Blueprint` is what we need to use.

To register a blueprint, the `register_blueprint()` method of the Flask application instance is used. When a blueprint is registered, any view functions, templates, static files, error handlers, etc. are connected to the application.

In each Blueprint package we make \_\_initII.py that has name information and imports routes. Routes further imports and links model and controller.

## Open doubts

- UserMixin?
- Why we pass Classes as param to Class?

## Making modules

- to get url_for use `module.route`. For eg: main.index. 
- But to render template use only `index.html` without module name. 

## Elastic Search

- You can install elastic search by `brew install elasticsearch` on mac.
- Access `http://localhost:9200` to view service JSON output.
- Also, install in python `pip install elasticsearch`
- To have launched start elasticsearch now and restart at login: `brew services start elasticsearch`
- Or, if you don't want/need a background service you can just run: `elasticsearch`

Todo: Search not working, fix it.