---
title: Understanding Flask
layout: post
categories: notes python
---

Flask is a microframework in Python. It is used to create a webapp. It can start a python web server. It can handle HTTP requests. It can also be used to make a webapp API.

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