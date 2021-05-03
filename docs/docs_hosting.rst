Hosting the Documentation
=========================

So far, we've been viewing our documentation locally on our machine. But
documentation is made for sharing!

Let's commit and push your documentation. I will be using `GitHub`_ in my
examples below, however you can choose to push it on other platforms such as
`GitLab`_ or `BitBucket`_.

Files to commit to git
----------------------

You'll notice that when we run ``sphinx-quickstart``, Sphinx generated a whole
bunch of files for us. Additionally, there were a number of files getting
generated under the ``_build`` directory. You might wonder if you have to
commit all of these files.

Here's are the files you need to add and commit to your git repository:

- ``conf.py``

- ``make.bat``

- ``Makefile``

- All of the ``.rst`` files, basically all of the documentation you wrote

- Any custom files you created under ``_static`` or ``_templates`` directories.
  If those folders are empty, then you can ignore them.

You do not need to commit anything in ``_build`` directory.

(optional) Push to remote
-------------------------

This step is optional. If you're not comfortable pushing your documentation
right now, and want to do it at a later time, it's fine.

(optional) Host the documentation on ReadTheDocs
------------------------------------------------

I'm a fan of hosting documentation through `ReadTheDocs`_. (I'm a `Gold member`_).

Some benefits:

- It's free if your project is open source, i.e. available publicly on `GitHub`_,
  `GitLab`_, or `BitBucket`_

- You can enable "preview" builds, so `ReadTheDocs`_ can build your documentation
  from pull requests. You can easily review documentation changes without
  needing to pull and build the PR locally.

- It can build from your default/main branch. So you can keep your documentation
  up to date.

- It can also build PDF version of your documentation without needing to set
  up additional configuration.

Please follow the documentation at :doc:`sphinx-rtd-tutorial:read-the-docs`
on how to do it.

(optional) Hosting the documentation elsewhere
----------------------------------------------

To host your documentation elsewhere, you'll have to figure out a way
to have your documentation built, for example by running the ``make html``
command, perhaps as part of your CI. You'll then want to "serve" the
``_build\html``. For example, you may need to copy over the output of ``_build\html``
to the web server that hosts your documentation.

Here's an example instructions on how to `host your Sphinx documentation
on GitHub pages`_.

.. _ReadTheDocs: https://readthedocs.org/

.. _Gold member: https://readthedocs.org/sustainability/

.. _GitHub: https://github.com

.. _GitLab: https://about.gitlab.com

.. _BitBucket: https://bitbucket.org

.. _host your Sphinx documentation on GitHub pages: https://www.docslikecode.com/articles/github-pages-python-sphinx/