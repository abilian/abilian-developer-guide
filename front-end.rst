Front-end
=========

References
----------

Since this section is a little short on content, here's a terrific list of recommendations:

- <https://github.com/bendc/frontend-guidelines/blob/master/README.md>

Also, this coding guide for HTML and CSS:

- <http://codeguide.co/>


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

We need to move our code base to a more modern, decoupled, archiecture.


Constraints
~~~~~~~~~~~

Like everyone who is doing front-end development, we have to deal with buggy browsers from the pasts.

UX
--

- <https://www.smashingmagazine.com/2010/02/designing-user-interfaces-for-business-web-applications/>
- <https://uxdesign.cc/ux-trends-2017-46a63399e3d2>
- <https://www.youtube.com/watch?v=wrlHi2jKw_Y>


JavaScript
----------

Embrace the future, now
~~~~~~~~~~~~~~~~~~~~~~~

We've used CoffeeScript in the past, but have reversed the decision to base all our front-end developments on CoffeeScript before it was put in practice.

We're now using ES6 aka ES2015 using the `Babel <https://babeljs.io/>`_ transpiler for our new projects (part of our existing code base is still based on ES5).

We plan to try using TypeScript in the future.


Libraries / frameworks
~~~~~~~~~~~~~~~~~~~~~~

We've used Angular on customers projects in the past.

Our current JavaScript framework of choice is `Vue.js <http://www.vuejs.org/>`_.


CSS
---

We're currently using Bootstrap (v3), because it's extremely popular and quite comprehensive.

We're using LESS (or SASS, depending on the phase of the moon).

We're also trying to find a way to write better (more manageable) CSS/LESS/SASS code to go along our pluggable architecture. The following posts (and all the references given therein) give a lot of interesting advice and point to several useful methodologies, that we should put to use:

- <https://github.com/jareware/css-architecture>
- <https://speakerdeck.com/mdo/at-mdo-ular-css>
- <https://medium.com/@fat/mediums-css-is-actually-pretty-fucking-good-b8e2a6c78b06>
- <https://mattstauffer.co/blog/organizing-css-oocss-smacss-and-bem>
- <http://benfrain.com/the-ten-commandments-of-sane-style-sheets/>
- <https://medium.com/@Heydon/things-to-avoid-when-writing-css-1a222c43c28f>
- <http://rscss.io/>


Patterns libraries aka style guides
-----------------------------------

Generalities:

- <http://www.designforfounders.com/style-tiles/>
- <https://www.smashingmagazine.com/taking-pattern-libraries-next-level/>
- <https://24ways.org/2016/designing-imaginative-style-guides/>

Specifics:

- <https://medium.com/ge-design/ges-predix-design-system-8236d47b089>
- <https://lightningdesignsystem.com/>
- <https://experience.sap.com/fiori-design-web/>
- <https://design.atlassian.com/>



Build tools
-----------

We're using NPM for package management, and WebPack for build.

WebPack provides live reloading (with the right extension) so that's cool.

Quality assurance
-----------------

JavaScript: We've started using `eslint` on some projects.

CSS: <http://benfrain.com/floss-your-style-sheets-with-stylelint/>

Unit tests: TODO.

Functional tests: we should be using Selenium (via Webdriver) more.

