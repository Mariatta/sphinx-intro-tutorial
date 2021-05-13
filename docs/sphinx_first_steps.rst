.. _quickstart:

Building a Documentation Project with Sphinx
--------------------------------------------

You need Python in order to install and start a `Sphinx`_ project.

For the purpose of this tutorial, we will be writing documentation
using `reStructuredText`_. If you're looking to use Markdown instead,
please go to this `documentation <https://www.sphinx-doc.org/en/master/usage/markdown.html>`_.

In this tutorial, we'll be working with `Sphinx`_ version 3.5.4.

.. _installation:

Installation
============

1. Within your project's repository, create a new directory where the documentation
   will live. For example, if you want the documentation to live under the ``docs``
   directory, create the ``docs`` directory:

   .. code:: bash

       $ mkdir docs


2. Within the ``docs`` directory, create and activate a Python virtual environment:

   .. code:: bash

       $ cd docs
       [../docs]$ python3 -m venv .env
       [../docs]$ source .env/bin/activate

3. Once within the virtual environment, install sphinx:

   .. code:: bash

       (.env)[../docs]$ python3 -m pip install -U pip Sphinx==3.5.4

4. Once you have Sphinx installed, run ``sphinx-quickstart``
   and answer the questions:

   .. code:: bash

       (.env)[../docs]$ sphinx-quickstart


Suggested answers
+++++++++++++++++

.. note:: You can press ``Enter`` to go with the default.


::

  > Separate source and build directories (y/n) [n]: n
  > Project name: Your project's name
  > Author name(s): Your name or your team's name
  > Project release []: Enter
  > Project language [en]: Enter


After you're finished, your ``docs`` directory should contain several files and
directories as follows::

    /_build/
    /_static/
    /_templates
    conf.py
    index.rst
    make.bat
    Makefile
    make.bat

Building documentation with Sphinx
==================================

Once you have `Sphinx`_ set up, you can build the documentation by typing ``make html`` command
on the terminal, within the ``docs`` directory, with the virtual environment activated.

.. code:: bash

    (.env)[../docs]$ make html

Once run, the documentation is generated under ``_build\html`` directory. Open the
``index.html`` file within the ``_build\html`` directory


Deactivate and activating virtual environment
=============================================

If you have a virtual environment, you can "exit" or deactivate it by typing
``deactivate`` from the command line:

.. code:: bash

    (.env)[../docs]$ deactivate


To activate the virtual environment again, which is needed to build the documentation
with Sphinx:

.. code:: bash

    [../docs]$ source .env/bin/activate


The index.rst file
==================

Locate the index.rst file within the ``docs`` directory. It should be created
after you run the ``sphinx-quickstart`` step.

It should look like the following::

  .. Intro to Sphinx documentation master file, created by
     sphinx-quickstart on .....
     You can adapt this file completely to your liking, but it should at least
     contain the root `toctree` directive.

  Welcome to Intro to Sphinx's documentation!
  ===========================================

  .. toctree::
     :maxdepth: 2
     :caption: Contents:




  Indices and tables
  ==================

  * :ref:`genindex`
  * :ref:`modindex`
  * :ref:`search``

Let's make some edit to the ``index.rst`` file. Add some text, any text, to the **space
above** the ``Indices and tables`` section. For example::

  Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam maximus condimentum
  fringilla. Phasellus cursus ligula eget diam faucibus, nec maximus metus ornare.
  Donec mi nulla, faucibus eu ante a, auctor iaculis arcu. Mauris orci mauris,
  mollis at orci sed, mattis sagittis urna. Etiam consectetur efficitur pellentesque.
  Donec tellus risus, suscipit non lorem in, ullamcorper gravida orci. Ut tristique
  vestibulum nisl et pharetra. Sed ac mollis arcu. Duis sit amet commodo massa.
  Quisque feugiat augue nulla, ut pretium nulla maximus in. Aliquam erat
  volutpat. Nunc feugiat mauris ac erat dictum aliquam consectetur ac elit.

  Indices and tables
  ==================

  * :ref:`genindex`
  * :ref:`modindex`
  * :ref:`search``


Save index.rst and re-build the documentation, by running ``make html`` in the
command line. Re-open ``index.html`` and you should see the lorem ipsum
paragraph appearing.

Adding more pages
=================

You'll probably have more than one page of documentation! Let's try adding a
few files.

Let's create several placeholder documentation files, for example: ``changelog.rst`` and
``tutorial.rst``.

Create both these files in the ``docs`` directory. The same directory where
your ``index.rst`` is.

**The newly created files cannot be empty!** Sphinx requires that you add at least
a **title** to each documentation page. So let's add some text to each of the file.

Content of ``changelog.rst`` file::

   Changelog
   =========


Content of ``tutorial.rst`` file::

   Tutorial
   ========

Save the files. Now let's add these two files into the Table of Contents in the
``index.rst`` file. Add the **filename** (without the .rst extension) of the
files you want to include, right under the ``toctree`` directive. Note that,
in `reStructuredText`_, whitespaces and indentation matters, just like in Python.
You need to add an extra line between the toctree and the list of files you're adding.

::

   .. toctree::
     :maxdepth: 2
     :caption: Contents

     tutorial
     changelog

Now save the ``index.rst`` file. Re-build the documentation by running ``make html``,
and reload your browser. You should see both Tutorial and Changelog reflected
in the Table of Contents, and you can click and navigate to them.


Autobuilding the Documentation
==============================

Authoring documentation this way can be a bit tedious and cumbersome,
since you have to always re-build the documentation by running ``make html`` and
then re-load your browser.

There is a way to automatically build your Sphinx documentation. Check out
the :ref:`autobuild-extension` section on how to set this up.



.. _reStructuredText: https://docutils.sourceforge.io/rst.html

.. _Sphinx: https://www.sphinx-doc.org/en/master/
