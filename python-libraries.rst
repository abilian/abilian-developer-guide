Libraries and Frameworks (Python)
=================================

TL;DR
-----

Here are the most important Python libraries we're using daily to develop the Abilian platform and projects:

-  Flask: http://flask.pocoo.org/
-  Bootstrap: http://twitter.github.com/bootstrap/
-  SQLAlchemy: http://sqlalchemy.org/
-  WTForms: http://wtforms.simplecodes.com/
-  Jinja 2 (for template makers): http://jinja.pocoo.org/docs/templates/

We are also using Django for one project we are maintaining (`COMT <http://www.co-ment.org>`_).


Intro and guidelines
--------------------

TODO.

Need a library: check there first <https://awesome-python.com/>, then PyPI.


Flask
-----

Flask is a micro web framework written in Python and based on the Werkzeug toolkit and Jinja2 template engine. It is BSD licensed.

The latest stable version of Flask is 0.11 as of June 2016. Applications that use the Flask framework include Pinterest, LinkedIn and the community web page for Flask itself

Flask is called a micro framework because it does not require particular tools or libraries. It has no database abstraction layer, form validation, or any other components where pre-existing third-party libraries provide common functions. However, Flask supports extensions that can add application features as if they were implemented in Flask itself. Extensions exist for object-relational mappers, form validation, upload handling, various open authentication technologies and several common framework related tools. Extensions are updated far more regularly than the core Flask program.

Reference:
~~~~~~~~~~

-  http://flask.pocoo.org/
-  Manuel PDF (250 pages)

Books and tutorials
~~~~~~~~~~~~~~~~~~~

- <https://exploreflask.com/>: Free Book, beginners level.
- <https://realpython.com/blog/python/flask-by-example-part-1-project-setup/>: blog series.
- <http://blog.miguelgrinberg.com/category/Flask>: huge blog series + <http://flaskbook.com/>: book by the same author.


Some insightful presentations:
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- <http://mitsuhiko.pocoo.org/pyladies.pdf>: very basic intro by Armin himself.
- <http://mitsuhiko.pocoo.org/flaskfun.pdf>: high level design considerations, but also some very useful code snippets.
- <https://speakerdeck.com/kennethreitz/flasky-goodness>
- <https://speakerdeck.com/mitsuhiko/advanced-flask-patterns>: must read (several times) once you've mastered the basics
- http://ua.pycon.org/static/talks/davydenko.pdf
- https://speakerdeck.com/jperras/large-scale-applications-with-flask-doing-more-with-less


Well-done projects:
~~~~~~~~~~~~~~~~~~~

-  https://github.com/hasgeek/ (Coaster, Eventframe, hasjob...)


SQLAchemy
---------

SQLAlchemy is an open source SQL toolkit and object-relational mapper (ORM) for the Python programming language released under the MIT License.

SQLAlchemy provides "a full suite of well known enterprise-level persistence patterns, designed for efficient and high-performing database access, adapted into a simple and Pythonic domain language". SQLAlchemy's philosophy is that SQL databases behave less and less like object collections the more size and performance start to matter, while object collections behave less and less like tables and rows the more abstraction starts to matter. For this reason it has adopted the data mapper pattern (like Hibernate for Java) rather than the active record pattern used by a number of other object-relational mappers. However, optional plugins allow users to develop using declarative syntax.

SQLAlchemy was first released in February 2006 and has quickly become one of the most widely used object-relational mapping tools in the Python community, alongside Django's ORM.

Reference:
~~~~~~~~~~

-  http://sqlalchemy.org/
-  Manuel PDF (560 pages)

Insightful articles
~~~~~~~~~~~~~~~~~~~

-  http://lucumr.pocoo.org/2011/7/19/sqlachemy-and-you/
-  http://www.aosabook.org/en/sqlalchemy.html

Presentations:
~~~~~~~~~~~~~~

-  http://techspot.zzzeek.org/files/2011/sqla_arch_retro.key.pdf
-  Several videos (search "Michael Bayer" on youtube or PyVideo.org).

More resources
~~~~~~~~~~~~~~

- <https://github.com/dahlia/awesome-sqlalchemy>

Jinja2
------

Jinja is a template engine for the Python programming language and is licensed under a BSD License created by Armin Ronacher. It is similar to the Django template engine but provides Python-like expressions while ensuring that the templates are evaluated in a sandbox. It is a text-based template language and thus can be used to generate any markup as well as sourcecode.

The Jinja template engine allows customization of tags, filters, tests, and globals. Also, unlike the Django template engine, Jinja allows the template designer to call functions with arguments on objects. Jinja is Flask's default template engine.

Doc for template designers is here: http://jinja.pocoo.org/docs/templates/


Werkzeug
--------

Werkzeug is the WSGI framework underlying Flask. It's normally not
needed to learn too much about it, but in case the doc is here:
http://werkzeug.pocoo.org/docs/

WTForms
-------

WTForms is a flexible forms validation and rendering library for python web development.

-  http://wtforms.simplecodes.com/


Babel
-----

Babel is an integrated collection of utilities that assist in internationalizing and localizing Python applications, with an emphasis on web-based applications.

Doc : <http://babel.pocoo.org/en/latest/>


Other libraries
---------------

Celery.

TODO.
