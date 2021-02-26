Introduction, vision and principles
===================================

About this document
-------------------

We are writing an `Employee Handbook` <http://en.wikipedia.org/wiki/Employee_handbook> for our current and future developers.

Here are some other similar document that have served as inspiration as we wrote this documents:

- <https://djaodjin.com/blog/guidelines.book.html>
- <https://github.com/thisissoon/Handbook>
- <http://playbook.thoughtbot.com/>


This doc is readable on <https://abilian-developer-guide.readthedocs.io/en/latest/>


Status
~~~~~~

This is a work in progress. Actually, what you are reading now is a very early draft.

Even if it was "finished" at some point, it should still be updated at least twice a year to reflect the evolutions of our business and of our technology choices.

Why is this document public?
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Why not? There are no trade secrets in this document.

Here are a few reasons:

- Hopefully, it will be useful to other people / companies.
- By publishing it, we hope to attract like-minded developers to strengthen our team.


Vision
------

About Abilian
~~~~~~~~~~~~~

`Abilian <http://www.abilian.com>`_ develops a software platform (also called Abilian), horizontal products (Abilian SBE = an Enterprise Social Networking platform, Abilian CRM = a CRM platform, etc.) and vertical products (ex: our software for competitiveness clusters, etc.).

The goals for the technical team are:

- To create a useful (for us and for external users / contributors) software platform. By useful, we mean that we, and others, can achieve greater productivity when developing products and projects.

- To create successful products and customer projects based on our platform. By successful, we mean that they are useful to our customers, and they sell well.


.. The perfect developer
   ~~~~~~~~~~~~~~~~~~~~~


Our open source projects
~~~~~~~~~~~~~~~~~~~~~~~~

We are the main developers of the following open source projects:

- `Abilian Core <https://github.com/abilian/abilian-core>`_
- `Abilian SBE <https://github.com/abilian/abilian-sbe>`_
- `OlaPy <https://github.com/abilian/olapy`_


Open source vs. customers projects
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

We are working both on public, open source, projects, and private projects for our customers (usually some customizations or extensions to our public projects).

When working on open source projects, we need to take a great care of not just making them successful technically, but also everything that will help them get other open source developers interested in the project.


Languages
~~~~~~~~~

We expect our developers to have knowledge of the following languages:

- Python 3
- JavaScript (ES6 and later)
- HTML
- CSS
- SQL
- RestucturedText and Markdown
- English


Principles
----------

Here is a short list of principles (or list of lists of principles) that should guide you when working at Abilian:

- Write code for others (including "future you"), not just for the computer.

- Minimize all feedback loops. This includes for instance:

  1. The time it takes to run the unit test suite (ideally, no more than a few seconds).
  2. The time it takes between a change in the code and a change in the web Browser.
  3. The time between a customer request and the moment it can be used.

- Practice Test-Driven Development (TDD).

  Why? For two reasons: 

  1. TDD (practiced correctly) helps come with better software design.
  2. It give us confidence that our product work properly, and that we can refactor them without fear of breaking things beyond repair.

- Practice "Documentation Driven Development", for public projects.

  1. Write documentation alongside the code. The simple act of trying to explain to others what we are trying to achieve with our software, and how, helps us clarify our thinking. If it's too hard to explain, then it's probably badly architected, designed or implemented.

  2. A simple variant is to practice "`README Driven Development <http://tom.preston-werner.com/2010/08/23/readme-driven-development.html>`_".

- Practice Domain Driven Design (DDD).

  See the Architecture & Design chapter in this document.

- To ease developments on modern hosting platforms (including our own servers), we've adopted the "Twelve Factor" principles, see: <http://12factor.net/>.

