---
title: SQLite and SQLAlchemy Notes
layout: post
categories: notes database
last_modified_at: 2020-07-15 13:31:18
---

## SQLite

- It is a micro database that can work in memory or a saved in file, eg, `store.db` .
- Queries are same as any other SQL.
- if `sqlite3` is installed then it opens a shell in command line, just like mysql shell.
- to open a file, use `.open FILENAME` to open an existing database.


## SQLAlchemy

- **ORMs** allow applications to manage a database using high-level entities such as classes, objects and methods instead of tables and SQL. The job of the ORM is to translate the high-level operations into database commands.
- It is an ORM not for one, but for many relational databases. SQLAlchemy supports a long list of database engines, including the popular MySQL, PostgreSQL and SQLite.

---

More on:
- [Flask SQL Alchemy](../flask-notes/#flask-sqlalchemy)