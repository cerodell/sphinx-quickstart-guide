Getting Started with Sphinx
===========================

.. meta::
   :description lang=en: Get started writing technical documentation with Sphinx and publishing to Read the Docs.


Sphinx is a powerful documentation generator that
has many great features for writing technical documentation including:

* Generate web pages, printable PDFs, documents for e-readers (ePub),
  and more all from the same sources
* You can use reStructuredText or Markdown
  to write documentation
* An extensive system of cross-referencing code and documentation
* Syntax highlighted code samples
* A vibrant ecosystem of first and third-party `extensions <https://www.sphinx-doc.org/en/master/usage/extensions/index.html>`_



Quick start
-----------

Assuming you have Python already, `install Sphinx <https://www.sphinx-doc.org/en/master/usage/installation.html>`_

*Recommend to use conda to install sphinx.*

.. code-block:: bash 

    conda install -c conda-forge sphinx

    or

    pip install sphinx

Create a directory inside your project to hold your docs:

.. code-block:: bash 

    cd /path/to/project
    mkdir docs

Run ``sphinx-quickstart`` in there:

.. code-block:: bash 

    cd docs
    sphinx-quickstart

This quick start will walk you through creating the basic configuration; in most cases, you
can just accept the defaults. When it's done, you'll have an ``index.rst``, a
``conf.py`` and some other files. Add these to revision control.

Now, edit your ``index.rst`` and add some information about your project.
Include as much detail as you like (refer to the `reStructuredText syntax <https://www.sphinx-doc.org/en/master/usage/restructuredtext/basics.html>`_
or `this template <https://www.writethedocs.org/guide/writing/beginners-guide-to-docs/#id1>`_ if you need help). Build them to see how they look:

.. code-block:: bash 

    make html

.. Your ``index.rst`` has been built into ``index.html``
.. in your documentation output directory (typically ``_build/html/index.html``).
.. Open this file in your web browser to see your docs.

.. .. .. figure:: /_static/images/first-steps/sphinx-hello-world.png
.. ..    :figwidth: 500px
.. ..    :target: /_static/images/first-steps/sphinx-hello-world.png
.. ..    :align: center

.. ..    Your Sphinx project is built

.. Edit your files and rebuild until you like what you see, then commit your changes and push to your public repository.
.. Once you have Sphinx documentation in a public repository, you can start using Read the Docs
.. by :doc:`importing your docs </intro/import-guide>`.


Using Markdown with Sphinx
--------------------------

You can use Markdown and reStructuredText in the same Sphinx project.
We support this natively on Read the Docs, and you can do it locally:

.. code-block:: bash 

    pip install recommonmark

Then in your ``conf.py``:

.. code-block:: python

   extensions = ['recommonmark']

.. warning:: Markdown doesn't support a lot of the features of Sphinx,
          like inline markup and directives. However, it works for
          basic prose content. reStructuredText is the preferred
          format for technical documentation, please read `this blog post`_
          for motivation.

.. _this blog post: https://www.ericholscher.com/blog/2016/mar/15/dont-use-markdown-for-technical-docs/


External resources
------------------

