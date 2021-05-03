.. Intro to Documentation with Sphinx and reStructuredText documentation master file, created by
   sphinx-quickstart on Sun May  2 12:31:31 2021.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to Intro to Documentation with Sphinx and reStructuredText's documentation!
===================================================================================


.. admonition:: info

   This tutorial was prepared for `PyCon 2021 <https://us.pycon.org/2021/schedule/presentation/23/>`_
   by `Mariatta <https://twitter.com/mariatta>`_.

Tutorial Description
--------------------

The success of Python and open source libraries is not separable from the
availability of good documentation. Reading documentation is one of the first
things a user of the open source library has to do.

In the Python open source community, documentation is often written using
reStructuredText markup language, and built with Sphinx. The official Python
documentation and Python Enhancements Proposals (PEPs) are all written using
reStructuredText. Being able to write documentation using reStructuredText
becomes a necessary skill for any aspiring Python open source contributors
and maintainers.

Yet, reStructuredText itself can be seen as a barrier into contributing to open
source, since it is not as straightforward as Markdown. Compared to Markdown,
reStructuredText is not as widely adopted outside of the Python community.
Don’t let this discourage you! Let’s break down this barrier! reStructuredText
is not as complicated as you might think. You can learn it!

In this tutorial, we'll go through various useful features of reStructuredText.
You will learn how to create and build a documentation project using Sphinx.
Not only will you learn a new skill, you can also confidently start contributing
to open source projects by helping to improve their documentation.

Agenda
------

.. csv-table::
   :header: "Topic", "Duration"

    "Introductions", "5 minutes"
    "Intro to reStructuredText and Sphinx", "10 minutes"
    "Build a Sphinx project", "10 minutes (assuming you've pre-installed prior to attending)"
    "First steps with reStructuredText", "20-30 minutes"
    "break", "15 minutes"
    "Using Sphinx Roles and Directives", "20-30 minutes"
    "Sphinx Extensions", "20-30 minutes"
    "break", "15 minutes"
    "Doc Hosting", ""
    "Common Issues, Q&A", ""


Code of Conduct
---------------

`PyCon`_'s Code of Conduct applies and will be enforced.

.. raw:: html

    <iframe src="https://github.com/sponsors/Mariatta/card" title="Sponsor Mariatta" height="225" width="600" style="border: 0;"></iframe>

.. toctree::
    :maxdepth: 2
    :caption: Contents:

    docs_in_python
    sphinx_first_steps
    rst_intro
    sphinx_roles
    sphinx_extensions
    docs_hosting

.. toctree::
    :maxdepth: 2
    :caption: Appendix:

    common_issues
    thanks
    license
    GitHub Repository <https://github.com/mariatta/sphinx-intro-tutorial>


.. toctree::
    :caption: Contributing:
    :hidden:


.. _PyCon: https://us.pycon.org/2021/about/code-of-conduct/