Libraries and Frameworks (Python)
=================================

TL;DR
-----

Here are the most important Python libraries we're using daily to develop the Abilian platform:

-  Flask: http://flask.pocoo.org/
-  Bootstrap: http://twitter.github.com/bootstrap/
-  SQLAlchemy: http://sqlalchemy.org/
-  WTForms: http://wtforms.simplecodes.com/
-  Jinja 2 (for template makers): http://jinja.pocoo.org/docs/templates/

We are also using Django for one project we are maintaining (`COMT <http://www.co-ment.org>`_).


Intro and guidelines
--------------------

TODO.


Flask
-----

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
- <https://speakerdeck.com/kennethreitz/flasky-goodness>
- <https://speakerdeck.com/mitsuhiko/advanced-flask-patterns>: must read (several times) once you've mastered the basics
- http://ua.pycon.org/static/talks/davydenko.pdf
- https://speakerdeck.com/jperras/large-scale-applications-with-flask-doing-more-with-less


Well-done projects:
~~~~~~~~~~~~~~~~~~~

-  https://github.com/hasgeek/ (Coaster, Eventframe, hasjob...)


SQLAchemy
---------

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


Jinja2
------

Flask default templating language, similar to Django's templates.

Doc for template designers is here: http://jinja.pocoo.org/docs/templates/


Werkzeug
--------

Werkzeug is the WSGI framework underlying Flask. It's normally not
needed to learn too much about it, but in case the doc is here:
http://werkzeug.pocoo.org/docs/

WTForms
-------

-  http://wtforms.simplecodes.com/


Babel
-----

- TODO: explain how to use Babel.


Other libraries
---------------

Celery.

TODO.
