.. _rst_intro:

reStructuredText
----------------

Now that we have a `Sphinx`_ project up and running, we want to start
writing some documentation. Let's get acquainted with reStructuredText!

Titles/Headings
===============

In Markdown, you'd add `#` signs in front of the text you want to turn into
headings.

In reStructuredText, you'd add underlines, like so::

   Section 1
   ---------

   Section 2
   ---------

   SubSection 2.1
   ==============

   SubSection 2.1.1
   ++++++++++++++++



.. note::

   You can use different characters of underlines, for example: ``-``, ``=``,
   ``+``. Headers with the same underline "style" will be rendered as the same
   level.

You can also add "overline", and it will be treated as yet a different level
of heading.

::

   ------------------
   Subsection 1.1.1.1
   ------------------

Links
=====

The syntax for links in reStructuredText is as follows::

    `Python Docs <https://docs.python.org>`_

Where ``Python Docs`` is the clickable text that appears on the rendered HTML,
and ``https://docs.python.org`` is the url.

.. note::
    Spacing is important here.
    There needs to be an empty space between the displayed text and the ``<`` sign.

So::

    `Python Docs<https://docs.python.org>`_

is not valid.

If you would be referencing the same urls multiple times in the same page,
you don't have to re-write the same urls again and again. You can declare a name
for it, for example::

   .. _Python Docs: https://python.org

Add that to the bottom of your ``.rst`` file. Then, anywhere in that file, you can
simply type ```Python Docs`_``, and at render time, it will automatically be
linked.


Text Emphasis
=============

Wrap text in single asterisks for italics text.::

    *italics*

Double asterisks to make it bold.::

    **bold**

Double-backticks for inline "code" formatting.::

   ``code``

Literal or Code Blocks
======================

Literal block is a block of  text where line breaks and whitespaces are significant
and preserved.
Add two colons ``::`` followed by a blank line. Then **indent** the text block
after it. The following text block will become literal block.

::

    ::

        Lorem ipsum dolor sit amet, consectetur adipiscing elit. In viverra convallis
        feugiat. Mauris facilisis dolor placerat massa porta vehicula. Vivamus quis
        posuere quam. Sed semper, libero vel tristique tincidunt, metus diam
        pellentesque dolor, congue dignissim nibh ipsum sed dui.


The ``::`` can be in a line of its own, or added at the end of the previous
paragraph's sentence. For example:

::

     This text will be formatted as usual, meanwhile::

        This passage will become literal block. Lorem ipsum dolor sit amet,
        consectetur adipiscing elit. In viverra convallis
        feugiat. Mauris facilisis dolor placerat massa porta vehicula. Vivamus quis
        posuere quam. Sed semper, libero vel tristique tincidunt, metus diam
        pellentesque dolor, congue dignissim nibh ipsum sed dui.

Code blocks works somewhat similar to a literal block. You can specify the
language, and you'll get the benefit of syntax highlighting using `Pygments`_.

Use the ``.. code::`` directive, followed by an empty line. Then, **indent**
your text block below it.

::

    .. code:: python

        from datetime import datetime
        print(datetime.now())


Lists
=====

Add asterisks or numbers in front of each list item. You can use `#.` to auto-number
the list items.

::

    * Bullet list item 1
    * Bullet list item 2
      If the list item text is too long, it can go to the next line, like this.

    1. Numbered list item 1
    2. Numbered list item 2

       1. Nested list item 2
       2. Nested list item 2

    #. Autonumbered list item
    #. Autonumbered list item


Documentation Comments
======================

You can write comment in reStructuredText. The comment will appear hidden
and not rendered. Add two dots (``..``) followed by a space, and the text
will become "comments".

::

    .. This line will not be rendered.

    ..
       You can have multiline comments, by adding indented text blocks.
       This line will not be rendered.

       This is still a comment.

Admonition
==========

There are a few "admonition" directives in reStructuredText, kind of like
a callout. For example if you want to have some text in a special callout box,
you can use the ``.. note::`` directive.

::

   .. note::
      Careful! Don't go overtime!

Will be rendered as:

.. note::
  Careful! Don't go overtime!

There are different kinds of admonitions, like ``.. attention::``,
``.. caution::``, and ``.. tip::``.

::

   .. danger::
       This step is dangerous! Be real sure about it!

Will be rendered as:

.. danger::
   This step is dangerous! Be real sure about it!

.. seealso::

   https://docutils.sourceforge.io/docs/ref/rst/directives.html#specific-admonitions


Tables
======

There are a few ways to render tables in reStructuredText.

Simple Table
++++++++++++

::

    ========  ========  ========
    Column A  Column B  Column C
    ========  ========  ========
    row 1A    row 1B    row 1C
    row 2A    row 2B    row 2C
    ========  ========  ========

Will be rendered as:

========  ========  ========
Column A  Column B  Column C
========  ========  ========
row 1A    row 1B    row 1C
row 2A    row 2B    row 2C
========  ========  ========


Grid table
++++++++++


::

    +----------+----------+----------+
    | Column A | Column B | Column C |
    +==========+==========+==========+
    | row 1A   | row 1B   | row 1C   |
    +----------+----------+----------+
    | row 2A   | row 2B   | row 2C   |
    +----------+----------+----------+


CSV Table
+++++++++

::

   .. csv-table::
      :header: "Column A", "Column B", "Column C"

      "row 1A", "row 1B", "row 1C"
      "row 2A", "row 2B", "row 2C"


Table of Contents
=================

Use the ``.. contents::`` directive to automatically generate a
**Table of Contents** based on the section headers on your documentation.

::

   .. contents::


Rendering Image
===============

There is an ``.. image::`` directive for this.

::

    .. image:: path_to_image.jpg


.. seealso::

   `Details <https://docutils.sourceforge.io/docs/ref/rst/directives.html#image>`_
   on how to customize the image directive.


.. _Sphinx: https://www.sphinx-doc.org/en/master/
.. _Pygments: https://pygments.org/