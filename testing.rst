Testing
=======

Testing is very important. If it's not tested, it's broken.



Unit testing
------------

Unit tests should be fast (less than a few seconds to run a full test suite).

They should use py.test because it's our testing framework of choice.



Integration testing
-------------------

TODO.


Front-end testing
-----------------

When developing SPA (single page applications), use your framework of choice 
prefered testing tools to implement unit and integration tests.


Full stack testing
------------------

To run full stack (back end + front end) integration testing, use Selenium or
a variant of it (or phantomjs / casperjs / ...).

Use the "page object pattern":
<https://nulogy.com/who-we-are/company-blog/articles/using-the-page-object-pattern-in-your-automated-tests/>
to make your test cleaner an maintainable.

Best practices can be explored at SeleniumConf (for instance: <http://2016.seleniumconf.co.uk/>).


