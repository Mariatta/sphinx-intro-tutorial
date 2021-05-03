Documentation in Python Open Source Community
=============================================

When we discuss documentation in the Pyrhon open source community, you'll probably
hear of these terminologies: `Docutils`_, `reStructuredText`_,
and `Sphinx`_.

What exactly are these?

reStructuredText
----------------

Think of `reStructuredText`_ as a **markup language**. You might already be familiar
with other markup language such as HTML or Markdown. In `Markdown`_, as you write
your text and document, you can specify ways to format or mark up your text,
and the `Markdown`_ can then be converted into HTML file, which you can later view
in the browser.

`reStructuredText`_ works the same way. You can write your text with certain
formatting and markup, and it can then be converted into HTML for viewing. The
file extension is ``.rst``.

`reStructuredText`_ predates `Markdown`_. Python has been using reStructuredText
since 2002. `Markdown`_ only came into existence two years later in 2004.

The Python community saw the need to have better formatting for their docstrings,
because the plaintext was not expressive enough.

With the acceptance of :pep:`287`, `reStructuredText`_ was adopted for the use
of Python docstrings.

Since then, `reStructuredText`_ has been used widely in Python, not just for
docstrings, but also in the official Python documentation as well as the PEPs
(Python Enhancement Proposals).

Many Python open source libraries are also using reStructuredText to author
their documentation, for example: `PyPA/packaging`_, `requests`_, `black`_.

GitHub and GitLab both supports rendering reStructuredText on their web UI.
For example, you can create ``readme.rst`` on your project, instead of the default
``readme.md``, and it can be rendered accordingly.

.. seealso::

    :pep:`287` reStructuredText Docstring Format

Docutils
--------

`Docutils`_ is the utility tool that can convert plain text documents (including
reStructuredText) into other useful formats, like HTML, XML or LaTeX.

`Docutils`_ is written in Python and is open source. The only dependency you need
in order to use it, is Python itself.

Sphinx
------

If `Docutils`_ is the tool that converts reStructuredText into HTML, then Sphinx
is like the engine that can take your various documentation files into an intelligent
and complete Documentation **project**.

`Sphinx`_ uses `Docutils`_ internally to parse reStructuredText. Sphinx has
additional features, like: **cross-referencing**, **indexing**, and
**hierarchial structure**.

Understanding the tooling like `reStructuredText`_ and `Sphinx`_ becomes an
indispensable skill for any Python open source contributors.

Sphinx and Markdown
-------------------

You can use Markdown with Sphinx, starting in Sphinx 2.1. Please read the
`documentation <https://www.sphinx-doc.org/en/master/usage/markdown.html>`_ on
how to configure Sphinx with Markdown.

.. _Docutils: https://docutils.sourceforge.io/

.. _reStructuredText: https://docutils.sourceforge.io/rst.html

.. _Sphinx: https://www.sphinx-doc.org/en/master/

.. _Markdown: https://daringfireball.net/projects/markdown/

.. _PyPA/packaging: https://packaging.python.org/

.. _requests: https://docs.python-requests.org/en/master/

.. _black: https://black.readthedocs.io/en/stable/
