Using Markdown with Sphinx
============================

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

