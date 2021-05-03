Sphinx Directives and Roles
===========================

Everything in the :ref:`rst_intro` section before, is built-in features
of reStructuredText. Those can be parsed by `Docutils`_ without needing `Sphinx`_.

In this section, we'll learn about the Sphinx-specific roles and directive.

You will need to have `Sphinx`_ for these to work.

Cross-referencing
-----------------

One of the Sphinx features that I appreciate the most is the ability to do
cross-referencing, which is being able to provide links from one page
of documentation to another page.

For example, suppose I have an installation guide within my documentation.
From other pages of my documentation, I may want to easily refer to
the installation guide. This is called "cross-referencing".

Cross-referencing is accomplished by two elements: a ``target`` and the
``reference`` role.

First, declare a ``target`` or ``label``, which works like a "bookmark". And the syntax
may look familiar to you by now; this is how you'd "name" your links.

In the documentation where I have my Installation Guide written, I'd add the
following "target" or "label".

::

   .. _install-guide:

   Installation Guide
   ==================

   Step 1: Create and activate a virtual environment
   Step 2: pip install it


Now, anywhere within my documentation, I can add ``:ref:`install-guide```.
When the documentation is built, ``:ref:`install-guide``` will be replaced
with a link to the ``Installation Guide`` section of the documentation.

Cross-referencing documentation pages
-------------------------------------

Use the ``:doc:`` role to cross-reference another page, as opposed to a specific
section, like what the ``:ref:`` role does.

::

    :doc:`license`
    :doc:`docs_in_python`
    :doc:`Custom Docs title <docs_in_python>`

Will render the following links:

:doc:`license`

:doc:`docs_in_python`

:doc:`Custom Docs title <docs_in_python>`

Downloadable Files
------------------

If you want to create a link to a downloadable content, i.e. things that cannot
be viewed or rendered on the browser, like a zip file, you can use
the ``:download:`` role.

::

    Download :download:`this Makefile <../make.bat>`

.. seealso:: More details on `Sphinx Roles`_.


.. _Docutils: https://docutils.sourceforge.io/

.. _reStructuredText Primer: https://www.sphinx-doc.org/en/master/usage/restructuredtext/basics.html#hyperlinks

.. _Sphinx: https://www.sphinx-doc.org/en/master/

.. _Sphinx Roles: https://www.sphinx-doc.org/en/master/usage/restructuredtext/roles.html#xref-syntax
