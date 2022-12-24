---
title: Notepad Public
---

Staging area - Start with H1, later move to `term-notes.md`

# Android Notes

ADB is utility to interact with android phone. It can install/uninstall apks. change connections etc.
 All commands here, [adb shell](https://adbshell.com/).

Enable Developer Options > USB Debugging

adb must be installed on your mac/pc.

Uninstall blotwares

- `adb devices` see your device
- `adb shell` enter phone shell
- `pm uninstall -k --user 0 com.mipay.wallet.in` to use pm is pkg mgr, and uninstall an app.

References:

- <https://forum.xda-developers.com/t/uninstall-system-apps-without-root-vivo-bloatware.3817230/>
- <https://technastic.com/vivo-bloatware-preinstalled-apps-list/>



## Easy Soft Sys

Color Pallet:

- Blue - #00a1e7, rgb(0,161,231) <https://www.colorhexa.com/00a1e7>
- Grey - #3f3f3f, rgb()
- Orange - #e74600, rgb(231,70,0)

Font: Gill Sans Nova Extra Condensed Bold

## Bookdown

Quick [getting started](http://seankross.com/2016/11/17/How-to-Start-a-Bookdown-Book.html).

Steps:

- `mkdir bookdown`
- `cd bookdown/`
- `git clone https://github.com/seankross/bookdown-start`
- `cd bookdown-start/`
- `r`
- `bookdown::render_book("index.Rmd")`

- all `# heading 1` are chapters.
- Add `Part I` before a chapter to make it part in a book, `# (PART) Data Science {-}`
- `> options(bookdown.render.file_scope = FALSE);` to use parts in diff directories.

To support GitHub flavoured MarkDowm, you need to add the following line to `_output.yml` file:

`md_extensions: +lists_without_preceding_blankline+pipe_tables+raw_html+emoji`

**Working on a book:**

- All mds are in `./data_science` folder.
- All images are in `./images` folder.
- Add new md file to `./_bookdown.yml` file. It also has index order.
- To build and run:
  - `r`
  - `bookdown::render_book("index.Rmd")`
  - new site availabe at `./docs/index.html`
  - `quit()` to exit R shell


References:

- Bookdown [cookbook](https://bookdown.org/yihui/rmarkdown-cookbook/rmarkdown-anatomy.html)
- [Bookdown](https://bookdown.org/yihui/bookdown/html.html)
- Rafalab [dsbook](https://rafalab.github.io/dsbook/introduction-to-productivity-tools.html)
- Rafalab book [source github](https://github.com/rafalab/dsbook/blob/master/_bookdown.yml).
- Bookdown data science notes [book](https://bookdown.org/mpfoley1973/data-sci/)
- Python Visualizations in [bookdown](https://bookdown.org/jamie/python_visualisation/)
- Using [Python Environments](https://bookdown.org/yihui/rmarkdown/language-engines.html)
- Show plotly html js in Rmarkdown [stackoverflow](https://stackoverflow.com/questions/50191208/display-python-plotly-graph-in-rmarkdown-html-document)
- code options [cheat sheet](https://rstudio.com/wp-content/uploads/2015/02/rmarkdown-cheatsheet.pdf)
- publishing on [github](https://bookdown.org/yihui/bookdown/github.html)
- pandoc markdown [formats](https://pandoc.org/MANUAL.html).


# Digital Marketing Notes

Instagram page earning:

- original images
- regular posting

Instagram Bot:

- Scrapper - <https://towardsdatascience.com/increase-your-instagram-followers-with-a-simple-python-bot-fde048dce20d#:~:text=Open%20a%20browser%20and%20login,users%20you%20followed%20using%20the>
- Post - <https://www.youtube.com/watch?v=vnfhv1E1dU4>


# Tableau



## Writeback in Tableau

## Mega String

"( '"
+[CC interaction_artifact_ID]
+"', '"
+[CC Status]
+"', '"+[CC Note]+"', '"+USERNAME()+"' )"

## HideInsert

[CC W InsertRun] = 0

## HideReset

[CC W InsertRun] = 4

## IncrementAdd

[CC W Incrementer]+1

## zero

0

## One

1

## Blank

""

## sheet reset

Saved successfully!
Go To Flow View ⮞

## Seet Sumbit

Submit ⮟

## CC Submitted

Writeback proc source

## Actions on form

select - reset - go to - next

select - reset - set - insertrun to 0

select - submit - set - cc mega string

select - submit - set - increment to +1

select - submit - set - insetRun 1

## actions on table sheet

select - table - set - insertRun 1

select - table - set - string blank

select - table - set - id to row selected





# Plotly D3 Vizs

- poltly built on top of D3
- python api uses plotly.js


Plotly Library:

- data - result of go.chartType(x=, y=, others=....)
- layout - title, axis, annotations
  - has param `updatemenus`
  - There are four possible update methods:
    - "restyle": modify data or data attributes
    - "relayout": modify layout attributes
    - "update": modify data and layout attributes
    - "animate": start or pause an animation
- frames: used for animations
  - we can add different frames to a chart
  - this can be used to produce the animations
  - Example can be found [here](https://plotly.com/python/animations/#frames).
- figure - final object combining data and layout.

Dash is putting and linking many plotly charts together.

## Other plotly products

Dash:

- Dash is Python framework for building *analytical web applications*.
- It is built on Flask, Plotly.js and React.js
- Just like flask, we define `app = dash.Dash()` and then at end `app.run_server()`
- We can create complete site with links.
- It has intractable story.

Chart Studio

- is like Tableau web edit and public.
- Can create and host data, charts and dashboards.
- can explore other people's work.
- charts are interactable and linked together.
- can be reverse engineered.
- can host notebooks as well.

ObservableHQ:

- Live, web edit, d3 notebooks.
- markdown and JS blocks
- lots of d3 features. like counts, action buttons etc
- can make dasboard as well.


References:

- [How and why I used Plotly (instead of D3)](https://www.freecodecamp.org/news/how-and-why-i-used-plotly-instead-of-d3-to-visualize-my-lollapalooza-data-d48345e2ca68/)
- [4 interactive Sankey diagrams made in Python](https://medium.com/plotly/4-interactive-sankey-diagram-made-in-python-3057b9ee8616)

# D3

Add D3 library. Then specific module.

- it is collection of module that work together
- data is bounded to the selections, it join-by-index
- By default, the data join happens by index: the first element is bound to the first datum, and so on. Thus, either the enter or exit selection will be empty, or both. If there are more data than elements, the extra data are in the enter selection. And if there are fewer data than elements, the extra elements are in the exit selection.
- selectAll() data() enter() append() - to add elements, SDEA.
<https://observablehq.com/@d3/d3-hierarchy?collection=@d3/d3-hierarchy>



# YouTube Channel Notes

Start creating a web of terms , make understand each thing, chamkao cheezo ko.
makeit understnad to 6yr old guy
start from docs, make reading a habit, start taking notes.
math teacher lessongs, i see, i do, i ...
small age learn, big understand, then decision.

Follow:

- miguel grinberg - <https://twitter.com/miguelgrinberg>
- Claudio Bernasconi - <https://twitter.com/CHBernasconiC>

# Mac OS (Linux) Ubuntu Notes

- `alias vynote="subl ~/path/to/file/notepad.txt"` add to `.bash_profile` to make shortcut
- cheat book - <https://github.com/0nn0/terminal-mac-cheatsheet#english-version>


# Python web app development

# Notes - 20221224

## Flask

All Flask applications must create an `application instance` (object of class Flask). The web server passes all requests it receives from clients to this object for handling, using a protocol called Web Server Gateway Interface (WSGI).

`app = Flask(__name__)` name is passed to Flask class constructor so it knows the location of app and hence can locate static and template.

Web Browser --request--> web server --> Flask app instance --route--> function to execute

`View Functions` handle application URL.

**Request** from client has lot of information in it, like header, user-agent, data etc. This information is available in `request object` and is made available to a `view-route function` to handle it. This object is not passed as an argument to function, rather it is made available using `contexts`. **Contexts** let certain objects to globally accessible, but are not global variable. They are globally accessible to only one thread. There can be multiple threads serving multiple requests from multiple client.

There are two contexts in Flask

- `current_app` variable in Application context, has info of active application.
- `g` variable in Application context, temp access **during** handling of a request. It is reset once request is served. Holds app info hence app context.
- `request`, in request context, obj having client req data.
- `session`, in request context, a dictionary to store values that can be accessed in different requests from same session.

Flask, in backend, makes these availabe to thread before dispaching a request and removes after request is handled. Explicitly, `current_app` can be made availabe by invoking `app.app_context()`

[ ] How does flask differente requests and clients?

URL-maps can be seen using `app.url_map`

`/static/<filename>` is special route added by Flask to serve static files.

`Requst Object` has methods and attributes having info on method, form, args, cookies, files, remote_addr, get_data().

**Request Hooks** are functions that can execute code before or after each request is processed. They are implemented as decorators  (functions that execute on event). These are the four hooks supported by Flask:

- `before_request` - like authenticate
- `before_first_request` - only before the first request is handled. Eg, to add server initialization tasks.
- `after_request` - after each request, but only if no unhandled exceptions occurred.
- `teardown_request` - after each request, even if unhandled exceptions occurred.

`g` context global storage can be used to share data between hook and view functons.

**Response Object** - Response is returned by view-funciton as a string (usually HTML) along with `status code` but can alos contain headers. So rather than sending comma separated tuple values, flask lets create response onject using `make_response()`.

```python
from flask import make_response

@app.route('/')
def index():
    response = make_response('<h1>Some response with a cookie!</h1>')
    response.set_cookie('message', '51')
return response
```

`return redirect('http://www.example.com')` is a response with URL and status code 302, however Flask lets it do easily using `redirect()` method. Another such is `abort(404)` which is treted as exception.

**Templates** `return render_template('user.html', name=name)` is another return helper function that can make use of template, which is HTML code where dynamic content can be filled on execution.

{{ super() }}, includes code from parent block, uif overriding a block.

`@app.errorhandler` is decorator that lets return a view from template for error responses like 404 and 500.

```python
@app.errorhandler(404)
def page_not_found(e):
    return render_template('404.html'), 404

@app.errorhandler(500)
def internal_server_error(e):
    return render_template('500.html'), 500
```

- `url_for()` utility builds URL for view-function giving route from app-url-map. Eg:
  - `url_for('user', name='john', page=2, version=1)` would return `/user/john?page=2&version=1`, they are good to build dynamic URLs that can be used in templates.
  - `url_for('user', name='john', _external=True)` would return `http://localhost:5000/user/john`.
  - `url_for('static', filename='css/styles.css', _external=True)` would return `http://localhost:5000/static/css/styles.css`.

## Flask Extensions

Most extensions use app context to initialize themselve, eg:

```python
from flask_bootstrap import Bootstrap
app = Flask(__name__)
bootstrap = Bootstrap(app)
```

- **Bootstrap** - provides templates and blocks that can be used in Jinja2 Templates
  - installation `pip install flask-bootstrap`
  - eg, `{% extends "bootstrap/base.html" %}` - base.html does not exist but is available via extension. Others are `navbar`, `content`, `script`

  ```html
  {% block scripts %}
  {{ super() }} <!--includes base scripts too, else overrides-->
  <script type="text/javascript" src="my-script.js"></script>
  {% endblock %}
  ```

- **Moment.js Flask-Moment** - Localization of Dates and Times
  - server should send UTC, client should present in local time and formatted to region using JavaScript.
  - `Moment.js` is perfect for this and is available as flask extension. It can be used in Jinja2 template.
  - `pip install flask-moment`
  - include the script, `jQuery` is already attached as part of bootstrap

    ```html
    {% block scripts %}
    {{ super() }}
    {{ moment.include_moment() }}
    {% endblock %}
    ```

    ```python
    from flask_moment import Moment

    moment = Moment(app)
    
    return moment(datetime.utcnow()).format('LLL') # local time
    return moment(datetime.utcnow()).fromNow(refresh=True) # a few seconds ago..
    ```

### Forms

- **WTForms** - Object Oriented Form building, rendering and validations.
  - supports forms validation, CSRF protection, internationalization (I18N), rendering form and more for any Python framework, its generic. [WTForms](http://wtforms.simplecodes.com/).
  - Cons - It lets you build form in python and help validate it. It adds a extra learning curve than using HTML for the same. It same as ORM that you define things as class variables.
  - You have to build a template but can use `Form.field`
  - Pros - It lets you extend forms.
    - lets you show error easily without using `flash`.
  - Building
  
    ```python
    from wtforms import Form, BooleanField, StringField, validators

    class RegistrationForm(Form):
      username     = StringField('Username', [validators.Length(min=4, max=25)])
      email        = StringField('Email Address', [validators.Length(min=6, max=35)])
      accept_rules = BooleanField('I accept the site rules', [validators.InputRequired()])
    ```

- **Flask-WTF** integration of Flask and WTForms
  - Includes CSRF, file upload, and reCAPTCHA. You mostly have to use formats of WTForms but write less as few things are done automatically that are realted to Flask patter.
  - Form fields are Class variables with different field type
  - validator functions can help validate, liek `Email()`.
  - Link to [Flask-WTF](http://pythonhosted.org/Flask-WTF/)
  - Building

    ```python
    from flask import Flask, render_template, session, redirect, url_for

    @app.route('/', methods=['GET', 'POST'])
    def index():
      form = NameForm() # defined as OOP model
      if form.validate_on_submit(): # cheks POST and validates
        session['name'] = form.name.data
        return redirect(url_for('index')) # POST -> back to this function as GET
      return render_template('index.html', form=form, name=session.get('name')) # When GET
    ```

  - Rendering

    ```html
    <form method="POST">
    {{ form.hidden_tag() }}
    {{ form.name.label }} {{ form.name() }}
    {{ form.submit() }}
    </form>
    ```

    - You can use bootstrap and flask-wtf combine to avoid writing template code and just use

      ```html
      {% import "bootstrap/wtf.html" as wtf %}
      {{ wtf.quick_form(form) }}
      ```

### Databases

Python has packages for most database engines like MySQL, Postgres, SQLite, MongoDb etc. If not, you can use ORM that lets you use Python objects to do SQL operations, SQLAlchemy or MongoEngine are such packages.

- [Flask-SQLAlchemy](http://pythonhosted.org/Flask-SQLAlchemy/) is wrapper on [SQLAlchemy](http://www.sqlalchemy.org/). You have to use SQLAlchemy pattern but it helps by making things tied to Flask way like session of SQLAlchemy is tied to web-request of flask.

  - installation `pip install flask-sqlalchemy`
  - Initiation

    ```python
    from flask_sqlalchemy import SQLAlchemy
    app.config['SQLALCHEMY_DATABASE_URI'] = 'sqlite:///' + os.path.join(basedir, 'data.sqlite')
    app.config['SQLALCHEMY_TRACK_MODIFICATIONS'] = False
    db = SQLAlchemy(app) # Object for all ops
    ```

  - **Model** - It is a Class which represents application entities, like, User, Task, Author, Book etc.
    - `__tablename__ = 'users'`
    - It has attributes that represent column name. `name = db.Column(db.String(64), unique=True)`
    - **Relationships** To create ER in OOPs way `users = db.relationship('User', backref='role')`
      - `backref` adds a backreference to other models
      - `lazy` does not execute until you add executor.
        - add `lazy='dynamic'` to prevent query execution.
    - `db.create_all()` creates all tables if they dont exist

  - **Create** a new row
    - Create an Object of Class to build a new row. `user_john = User(username='john', role=admin_role)`
    - add - `db.session.add(user_john)`
    - `id` is added to object after `db.session.commit()commit()`
  - **Update** - `db.session.add()` also edits.
  - **Delete** - `db.session.delete(obj_name)`
  - **Read** - `query` object is avilable to all model class. It has filter-options and executors that build a SQL Query statement.
    - Filter-Options - `filter()`, `filter_by()`, `limit()`, `offset()`, `order_by()`, `group_by()`
    - Executors - `all()`, `first()`, `first_or_404()`, `get()`, `get_or_404()`, `count()`, `paginate()`
    - Examples
      - `User.query.all()` reads all records
      - `User.query.filter_by(role=user_role).all()`
    - `str(User.query.filter_by(role=user_role))` returns SQL query

  - **RAW SQL** - give your SQL statements
    - `db.session.execute(SQL)` returns cursor
    - `db.session.execute(SQL).all()` - returns List result set

  - **Shell Operations** - CRUD from Flask Shell
    - `flask --app hello.py shell` start shell with *app_context*, python shell will not have that.
    - `db.cratte_all()` creates SQLite file.

- **Migrations** DB changes version controlled
  - When DB is handled using ORM, all changes to DB is done via ORM. If you have to add a column it is added by ORM so it will delete the table and create new but to prevent data loss in table it will create a migration script to create and populate again.
  - `Flask-Migrate` is wrapper on `Alembic` a SQLAlchemy migration framework.
  - `pip install flask-migrate`
  - `from flask_migrate import Migrate`
  - `migrate = Migrate(app, db)`
  - `flask --app hello.py db init` migration directory, script is generated
  - `upgrade()` has data changes to be done in this migration
  - `downgrade()` rolls back to previous state
  - Steps to make a migration
    - Make changes to model classes
    - `flask --app hello.py db migrate -m "initial migration"` to generate script
    - review for accurate changes. add to source control
    - `flask--app hello.py db upgrade` to do migration in database

## GIT

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

- `git switch -c <new-branch-name>`

## Python

`Decorators` are a standard feature of the Python language. A com‐
mon use of decorators is to register functions as handler functions
to be invoked when certain events occur.

[ ] what is context in python

## Computer Science

A thread is the smallest sequence of instructions that can be man‐
aged independently. It is common for a process to have multiple
active threads, sometimes sharing resources such as memory or file
handles. Multithreaded web servers start a pool of threads and
select a thread from the pool to handle each incoming request.

### OOPS

- Object is a Class and has
  - `attributes` - variables
  - `methods()` - functions
