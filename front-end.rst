Front-end
=========

References
----------

Since this section is a little short on content, here's a terrific list of recommendations:

- <https://github.com/bendc/frontend-guidelines/blob/master/README.md>


Past, present, future
---------------------

Current state
~~~~~~~~~~~~~

Our front-end code base (at least for Abilian Core and Abilian SBE) is currently composed of the following JavaScript libraries:

-  JQuery
-  Datatables: http://datatables.net/
-  Select2: http://ivaynberg.github.com/select2/

We're also using the Boostrap CSS framework (including some of its JavaScript extensions).

Where we are heading
~~~~~~~~~~~~~~~~~~~~

A lot have changed in the JavsScript world over the last three years, since we've started the Abilian project (and company).

While the "jQuery + plugins + spaghetti code" approach that we've been using so far is probably enough for the kind of interaction we're featuring currently, it's now time to be more ambitious with our front-end code.

Now is it time to embrace a more decoupled architecture? TODO: discuss pros and cons.


Constraints
~~~~~~~~~~~

Like everyone who is doing front-end development, we have to deal with buggy browsers from the pasts.


JavaScript
----------

Embrace the future, now
~~~~~~~~~~~~~~~~~~~~~~~

We've used CoffeeScript in the past, but have reversed the decision to base all our front-end developments on CoffeeScript before it was put in practice.

In 2015, we plan to use ES6, first by leverage the recent works on the `Traceur <https://github.com/google/traceur-compiler>`_ and `Babel <https://babeljs.io/>`_ transpilers. Of course, these tools should be fully integrated with the development tools we are using, including:

- Seamless build and deployment to the browser (using, e.g., Gulp + Livereload).
- Source map support.
- IDE support (source code highlighting, syntax checker, autocompletion, etc.).


Libraries / frameworks
~~~~~~~~~~~~~~~~~~~~~~

We've used Angular on customers projects in the past, and may use it again in the future.

We're also watching what others are doing in this space, including, of course, React.


CSS
---

We're using Bootstrap, because it's extremely popular and quite comprehensive.

We're using LESS (or SASS, depending on the phase of the moon).

We're also trying to find a way to write better (more manageable) CSS/LESS/SASS code to go along our pluggable architecture. The following posts (and all the references given therein) give a lot of interesting advice and point to several useful methodologies, that we should put to use:

- <https://medium.com/@fat/mediums-css-is-actually-pretty-fucking-good-b8e2a6c78b06>
- <https://mattstauffer.co/blog/organizing-css-oocss-smacss-and-bem>


Front-end tooling
-----------------

TODO: use Gulp, Bower and/or WebPack.

TODO: live reloading.
