Front-end
=========

Update 2018
-----------

JavaScript
~~~~~~~~~~

We use eslint to keep our code tidy.

We may switch to TypeScript in the future.

We use prettier to auto-format our code, with appropriate plugins to format JS code inside HTML or Vue components.

We use Jest for tests.

VueJS
~~~~~

We now use VueJS for our new front-end projects.

Some references:

- Official Style Guide: <https://vuejs.org/v2/style-guide/>
- Testing: use <https://github.com/vuejs/vue-test-utils>
- Additional resources on testing:
  - <https://medium.com/pixelmatters/unit-testing-with-vue-approach-tips-and-tricks-part-1-b7d3209384dc>


References
----------

Since this section is a little short on content, here's a terrific list of recommendations:

- <https://github.com/bendc/frontend-guidelines>

Also, this coding guide for HTML and CSS:

- <http://codeguide.co/>


Past, present, future
---------------------

Current (aka old) state
~~~~~~~~~~~~~~~~~~~~~~~

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

Our framework of choice is now Vue.js.


Constraints
~~~~~~~~~~~

Like everyone who is doing front-end development, we have to deal with buggy browsers from the pasts.

UX
--

- <https://www.smashingmagazine.com/2010/02/designing-user-interfaces-for-business-web-applications/>
- <https://uxdesign.cc/ux-trends-2017-46a63399e3d2>
- <https://www.youtube.com/watch?v=wrlHi2jKw_Y>
- <http://ux.handson.co/>
- <http://www.designingsocialinterfaces.com/patterns/Main_Page> + associated book
- <https://medium.com/@kennycheny/the-best-user-experience-design-links-of-2016-46e472660a52>
- <https://en.99designs.fr/blog/tips/7-unbreakable-laws-of-user-interface-design/>
- <https://medium.com/@erikdkennedy/7-rules-for-creating-gorgeous-ui-part-1-559d4e805cda>
- <https://medium.com/@erikdkennedy/7-rules-for-creating-gorgeous-ui-part-2-430de537ba96>


JavaScript
----------

Embrace the future, now
~~~~~~~~~~~~~~~~~~~~~~~

We've used CoffeeScript in the past, but have reversed the decision to base all our front-end developments on CoffeeScript before it was put in practice.

We're now using ES6 aka ES2015 using the `Babel <https://babeljs.io/>`_ transpiler for our new projects (part of our existing code base is still based on ES5).

Here are some references regarding ES2015:

- <http://slides.com/drksephy/ecmascript-2015>
- <https://github.com/getify/You-Dont-Know-JS> (book series)
- <http://exploringjs.com/es6/>

We plan to try using TypeScript (a statically typed variant of JS) in the future.


Libraries / frameworks
~~~~~~~~~~~~~~~~~~~~~~

We've used Angular on customers projects in the past.

Our current JavaScript framework of choice is `Vue.js <http://www.vuejs.org/>`_.


Links
~~~~~

- <https://medium.com/@housecor/12-rules-for-professional-javascript-in-2015-f158e7d3f0fc>


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
- <https://github.com/edx/ux-pattern-library/wiki/Styleguide:-Sass-&-CSS>
- <http://alistapart.com/article/css-audits-taking-stock-of-your-code>
- <http://ecss.io/>
- <https://benfrain.com/the-ten-commandments-of-sane-style-sheets/>
- <https://sass-guidelin.es/>
- <https://philipwalton.com/articles/decoupling-html-css-and-javascript/>


Patterns libraries aka style guides
-----------------------------------

Generalities:

- <http://bradfrost.com/blog/post/style-guides/>
- <http://www.designforfounders.com/style-tiles/>
- <https://www.smashingmagazine.com/taking-pattern-libraries-next-level/>
- <https://24ways.org/2016/designing-imaginative-style-guides/>
- <https://www.springload.co.nz/blog/introduction-pattern-libraries/>

Specifics:

- <https://medium.com/ge-design/ges-predix-design-system-8236d47b089>
- <https://lightningdesignsystem.com/>
- <https://experience.sap.com/fiori-design-web/>
- <https://design.atlassian.com/>
- <http://dropbox.github.io/scooter/>
- <https://buffer.com/style-guide>

More here: <https://github.com/gztchan/awesome-design#style-guidebranding-octocat>


Build tools
-----------

We're using NPM for package management (and also YARN), and WebPack for build.

WebPack provides live reloading (with the right extension) so that's cool.

We **don't** use gulp or grunt.

- <https://medium.com/@dabit3/introduction-to-using-npm-as-a-build-tool-b41076f488b0>
- <https://yarnpkg.com/>
- <https://webpack.js.org/>


Quality assurance
-----------------

JavaScript: We've started using `eslint` on some projects.

CSS: <http://benfrain.com/floss-your-style-sheets-with-stylelint/>

Unit tests: TODO.

Functional tests: we should be using Selenium (via Webdriver) more.

