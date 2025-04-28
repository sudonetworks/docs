Example Sphinx RST File with Glossary
====================================

This file demonstrates how to create a glossary in reStructuredText using Sphinx.

Glossary
--------

.. glossary::
    Term 1
        Definition of term 1.  This can span multiple lines.

    Term 2
        Definition of term 2.

    Another Term
        A longer definition for another term.  This shows how
        definitions can be wrapped to multiple lines.

    Sphinx
        Sphinx is a tool that makes it easy to create intelligent and beautiful
        documentation.  It is often used for Python projects.

    reStructuredText (RST)
        reStructuredText is a plain text markup language, often used with
        Sphinx.

    Documentation
        The set of documents that describe a software project,
        API, or other subject.

    API
        Application Programming Interface. A set of definitions
        and protocols for how software components should interact.

Using Glossary Terms
--------------------

You can refer to terms defined in the glossary using the :term:`role`.
For example, we can refer to :term:`Sphinx`, :term:`reStructuredText (RST)`,
:term:`Documentation`, and :term:`API`.

You can also use a different text to refer to the term, like this:
:term:`RST <reStructuredText (RST)>`.

Another example :term:`Term 1` and :term:`Term 2`.

