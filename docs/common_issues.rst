.. _common-issues:

Common Issues
=============

Some common issues we've seen when building the documentation using `Sphinx`_

If you encounter a problem and have figured out the solution, feel free
to add to this list and share your knowledge.

1. ``quickstart.rst: WARNING: document isn't included in any toctree``

   This means you have a file called ``quickstart.rst`` but you did not reference
   it from within the ``toctree`` directive of ``index.rst``.

2. ``index.rst:9: WARNING: toctree contains reference to document 'fruits' that doesn't have a title: no link will be generated``

   You need to have at least one "title" element within the ``fruits.rst``, so that
   the table of contents can be generated appropriately.


Other troubleshooting tips
--------------------------

Remember that there are many Python open source projects out there that
uses Sphinx and reStructuredText as part of their documentation tooling.

Most of the time, you can see their documentation source to see how the doc was
written. Look for the "show source" link, usually at the footer of each Sphinx
documentation. The location might depends on the theme that they're using.

.. _Sphinx: https://www.sphinx-doc.org/en/master/
