Software Design and Architecture
================================


The "4 principles of simple design"
-----------------------------------

This short series of principles is easy to remember, but surprisingly deep.

A design is simple to the extent that it:

- Passes its tests
- Minimizes duplication
- Maximizes clarity (reveals its intent)
- Has fewer elements (classes/modules/packages...)

References:

- <http://www.jbrains.ca/permalink/the-four-elements-of-simple-design>
- <http://blog.thecodewhisperer.com/2013/12/07/putting-an-age-old-battle-to-rest/>


SOLID & GRASP
-------------

A solid grasp (or "SOLID GRASP", see below) of object oriented techniques is expected to work on the Abilian project.

SOLID means:

- `Single responsibility principle <http://en.wikipedia.org/wiki/Single_responsibility_principle>`_: a class should have only a single responsibility (i.e. only one potential change in the software's specification should be able to affect the specification of the class).

- Open/closed principle: software entities … should be open for extension, but closed for modification.

- Liskov substitution principle: "objects in a program should be replaceable with instances of their subtypes without altering the correctness of that program."

- Interface segregation principle: many client-specific interfaces are better than one general-purpose interface."

- Dependency inversion principle: one should “Depend upon Abstractions. Do not depend upon concretions."



Here are a few references:

- `SOLID <http://en.wikipedia.org/wiki/SOLID_(object-oriented_design)>`_ and `GRASP <http://en.wikipedia.org/wiki/GRASP_(object-oriented_design)>`_ (according to Wikipedia)
- See also: <http://nikic.github.com/2011/12/27/Dont-be-STUPID-GRASP-SOLID.html>


Domain Driven Design
--------------------

Domain-driven design (DDD) is an approach to software development for complex needs by connecting the implementation to an evolving model.[1] The premise of domain-driven design is the following:

- Placing the project's primary focus on the core domain and domain logic.
- Basing complex designs on a model of the domain.
- Initiating a creative collaboration between technical and domain experts to iteratively refine a conceptual model that addresses particular domain problems.

(Source: `Domain-driven design on Wikipedia <http://en.wikipedia.org/wiki/Domain-driven_design>`_).

These are very general (and important) principles, which we will develop in future version of this guide.

There are also important and useful principles on how to achitect and design you application. See below for some patterns.


Tactical patterns
~~~~~~~~~~~~~~~~~

Here is the list of the technical (or tactical) patterns that are relevant to DDD.

- Layered (or onion, or hexagonal) Architecture: "Isolate the expression of the domain model and the business logic, and eliminate any dependency on infrastructure, user interface, or even application logic that is not business logic."

- Entities: "When an object is distinguished by its identity, rather than its attributes, make this primary to its definition in the model. Keep the class definition simple and focused on life cycle continuity and identity."

- Value Objects: "When you care only about the attributes and logic of an element of the model, classify it as a value object. Make it express the meaning of the attributes it conveys and give it related functionality. Treat the value object as immutable."

- Domain Events: "Model information about activity in the domain as a series of discrete events. Represent each event as a domain object. These are distinct from system events that reflect activity within the software itself."

- Domain Services: "When a significant process or transformation in the domain is not a natural responsibility of an entity or value object, add an operation to the model as a standalone interface declared as a service."

- Modules: "Choose modules that tell the story of the system and contain a cohesive set of concepts. Give the modules names that become part of the ubiquitous language."

- Aggregates: "Cluster the entities and value objects into aggregates and define boundaries around each. Choose one entity to be the root of each aggregate, and allow external objects to hold references to the root only (references to internal members passed out for use within a single operation only)."

- Repositories: "For each type of aggregate that needs global access, create a service that can provide the illusion of an in-memory collection of all objects of that aggregate’s root type."

- Factories: "Shift the responsibility for creating instances of complex objects and aggregates to a separate object, which may itself have no responsibility in the domain model but is still part of the domain design."

Some of these patterns may look a bit scary for a Python developer at first, but they make sense. See `Deliver Domain Driven Design Dynamically <http://goo.gl/BvTcHJ>`_ for a good discussion.


Other patterns
~~~~~~~~~~~~~~

See Eric Evans' book and/or the Domain-Driven Design Reference below.


References
~~~~~~~~~~

- `Domain-Driven Design Reference <https://domainlanguage.com/ddd/patterns/DDD_Reference_2011-01-31.pdf>`_.
- `Deliver Domain Driven Design Dynamically <http://goo.gl/BvTcHJ>`_ (talk about DDD in Python).
- `DDD with Ruby <http://virtual-genius.com/presentations/ddd_with_ruby_20130614.html>`_.
- `DDD in Ruby <http://victorsavkin.com/ddd>`_.
- `Code in the Language of the Domain <http://programmer.97things.oreilly.com/wiki/index.php/Code_in_the_Language_of_the_Domain>`_ (short, but profound)


Hexagonal Architecture (aka "Ports & Adapters", aka "Onion Ar")
-----------------------------------------------

(Also known as "Ports & Adapters" or "Onion Architecture").

Here's a high level view of how we should structure our framework:

- <http://blog.8thlight.com/uncle-bob/2012/08/13/the-clean-architecture.html> (+ all the references in the text).
- <http://alistair.cockburn.us/Hexagonal+architecture>

This architectural principle is compatible with DDD (see: <http://www.infoq.com/news/2014/10/ddd-onion-architecture>).

Additional references:

- <http://fideloper.com/hexagonal-architecture> (for PHP)
- <http://victorsavkin.com/post/42542190528/hexagonal-architecture-for-rails-developers> (for Rails)


Test Driven Development
-----------------------

Motivation and principles
~~~~~~~~~~~~~~~~~~~~~~~~~

After seeing Gary Bernardt video "`Slow test / fast test <http://www.youtube.com/watch?v=RAxiiRPHS9k>`_" (see also `this report <https://pycon-2012-notes.readthedocs.org/en/latest/fast_tests_slow_tests.html>`_ on the same talk), I'm convinced that it's important to have unit tests that pass as fast as possible (< 1 sec!), and possibly slower tests that are not run as often.

Our approach should be to distinguish between different tests classes:

- unit tests (in tests/unit), that test classes mostly in isolation, using mocks or stubs if needed.

- integration tests (in tests/integration), that test integration of actual components (no mocks).

- functional web tests, that test the web apps using the web interface, either using a browser (Selenium / WebDriver) or that leverage the framework to a similar effect.

- functional web API tests, that thoroughly test a web API using either an external tools (ex: FunkLoad) or the testing framework provided by Flask.

- load tests, using something like FunkLoad.

- system tests, that test the full system (in a VM), including upgrade scenarios.

At this point, functional tests are merged with integration tests, and system and load tests are non-existent.

We should aim for at least 80% measurable line coverage.


Tools for Test Driven Development
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

We're using py.test as our primary test runner and test framework, as we believe it to me the most "pythonic" of all testing frameworks (much more so that the standard library's ``unittest`` module, which is clearly heavily influence by Java and indirectly SmallTalk). This was not always the case, so we plan to migrate our tests progressively to fully leverage py.test as a testing framework (and not just a test runner).

TODO: 

- Links to pytest docs & tutorials.
- Mocking
- Web testing

(Or move this section to other chapters.)


API design
----------

As library / frameworks author, we must be extra careful wrt the quality of our API. A good project should have APIs that are stable (so if you make a mistake, you must live with it for a long time), easy to use and remember, etc.

- <http://qt-project.org/wiki/API_Design_Principles>
- <http://lcsd05.cs.tamu.edu/slides/keynote.pdf>
- <http://pyvideo.org/video/1705/api-design-for-library-authors>

This is both true for "regular" API (in whatever language we are working on) and for "Web" API.

For Web API, we're promoting the REST architectural style.


Books
-----

A few books relevant to this subject:

- Patterns of Enterprise Application Architecture (Martin Fowler)
- Refactoring (Martin Fowler)
- Domain Driven Design (Eric Evans)
- Growing Object-Oriented Software, Guided by Tests (Steve Freeman et Nat Pryce)
- Object Design: Roles, Responsibilities, and Collaborations (Rebecca Wirfs-Brock; Alan McKean)




