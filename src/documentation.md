# Documentation

Good developers don't just write code, they also write good documentation alongside the code.

## Principles

Given the tools we are using, the following principles should be applied:

1. We should treat the documentation as a first-class deliverable of our software. When you write a public API for a module, always build the doc as you develop and check that the doc makes sense.
2. It's important to treat both the narrative part and the API part properly. If you document only your API, as some developers do, this won't be enough to get potential users on board with our efforts.
3. For the API part, one should document all the public parts (classes, methods, attributes, functions) of the API, and nothing else, with proper docstrings.

Examples of outstanding documentation (among many others) include: [Flask](http://flask.pocoo.org/docs/), [SQLAlchemy](http://docs.sqlalchemy.org/en/) and [scikit-learn](http://scikit-learn.org/stable/documentation.html).

## Comments

> *A delicate matter, requiring taste and judgment. I tend to err on the
> side of eliminating comments, for several reasons. First, if the code is
> clear, and uses good type names and variable names, it should explain
> itself. Second, comments aren't checked by the compiler, so there is no
> guarantee they're right, especially after the code is modified. A
> misleading comment can be very confusing. Third, the issue of typography:
> comments clutter code.* -- Rob Pike

- \<<http://ericholscher.com/blog/2017/jan/27/code-is-self-documenting/>>
- \<<https://dev.to/raddikx/dont-document-your-code-code-your-documentation>>

## Tools

For Python software, we use [Sphinx](http://www.sphinx-doc.org/en/stable/) to generate documentation from both standalone texts, and text embedded in the code (using Docstrings).

See: \<<http://ericholscher.com/blog/2016/jul/1/sphinx-and-rtd-for-writers/>>

This means that our documentation is written using the RestucturedText (ReST) language. This cheat sheet can be useful:

\<<http://github.com/ralsina/rst-cheatsheet/raw/master/rst-cheatsheet.pdf>>

BTW, we're not using Markdown (or just parcimonuously) for reasons outlined there: \<<http://ericholscher.com/blog/2016/mar/15/dont-use-markdown-for-technical-docs/>>.

We publish our documentation on [ReadTheDoc](https://readthedocs.org/).

The `README.rst` files at the root of our projects are also extremely important (as they are often the first things that people read when discovering our projects, either on GitHub or on PyPI).

### Specific recommendations regarding Sphinx

For Sphinx to produce outstanding documentation, we need to pay attention to the way we write docstrings.

We should use the [Napoleon](http://sphinx-doc.org/latest/ext/napoleon.html) Sphinx plugin.

See the following links (from the Napoleon doc) for additional recommendation:

- \<<https://github.com/numpy/numpy/blob/master/doc/HOWTO_DOCUMENT.rst.txt>>
- \<<https://github.com/Khan/style-guides/blob/master/style/python.md#docstrings>>

## References & tips

- \<<http://docs.python-guide.org/en/latest/writing/documentation/>>
- \<<http://ericholscher.com/blog/2014/feb/27/how-i-judge-documentation-quality/>>
- \<<http://docs.writethedocs.org/>>
- \<<http://docness.readthedocs.io/>>
- \<<http://jacobian.org/writing/great-documentation/>>
- \<<https://speakerdeck.com/ogrisel/documentation>>
- \<<https://medium.com/@limedaring/five-tips-for-improving-your-technical-writing-and-documentation-47353723c8a7>>
