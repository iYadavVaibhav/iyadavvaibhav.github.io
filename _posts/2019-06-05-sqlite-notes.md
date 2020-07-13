---
title: SQLite and SQLAlchemy Notes
layout: post
categories: notes database
---

## SQLite

- It is a micro database that can work in memory or a saved in file, eg, `store.db` .
- Queries are same as any other SQL.
- if `sqlite3` is installed then it opens a shell in command line, just like mysql shell.
- to open a file, use `.open FILENAME` to open an existing database.


## SQLAlchemy

- **ORMs** allow applications to manage a database using high-level entities such as classes, objects and methods instead of tables and SQL. The job of the ORM is to translate the high-level operations into database commands.
- It is an ORM not for one, but for many relational databases. SQLAlchemy supports a long list of database engines, including the popular MySQL, PostgreSQL and SQLite.

### Flask-SQLAlchemy

- It is an extension for Flask that adds support for SQLAlchemy to your application. 
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