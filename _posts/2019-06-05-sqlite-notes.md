---
title: SQLite and SQLAlchemy Notes
layout: post
categories: notes database
---

## SQLite

It is a micro database that can work in memory or a file.

Queries are same as any other SQL.

sqlite3 opens a shell in command line.

`.open FILENAME` opens an existing database.


## SQLAlchemy

**ORMs** allow applications to manage a database using high-level entities such as classes, objects and methods instead of tables and SQL. The job of the ORM is to translate the high-level operations into database commands.

The nice thing about SQLAlchemy is that it is an ORM not for one, but for many relational databases. SQLAlchemy supports a long list of database engines, including the popular MySQL, PostgreSQL and SQLite.


**Flask-SQLAlchemy** is an extension for Flask that adds support for SQLAlchemy to your application. 