Markdown with Sphinx
============================

Markdown and reStructuredText can be used in the same Sphinx project.

If you haven't done so you'll first need to install ``recommonmark`` and add it to your extensions in your ``conf.py``

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


Add a Markdown page to toctree
+++++++++++++++++++++++++++++++++

In the ``source/`` folder make a file call ``mymarkdown.md``

.. code-block:: bash

    touch mymarkdown.md

Open ``mymarkdown.md`` and add a header and some other conectent

This code came from https://markdown-it.github.io/

.. code-block::

    # Example Markdown

    ## h2 Heading
    ### h3 Heading
    #### h4 Heading
    ##### h5 Heading
    ###### h6 Heading


    ## Horizontal Rules

    ___

    ---

    ***


    ## Typographic replacements

    Enable typographer option to see result.

    (c) (C) (r) (R) (tm) (TM) (p) (P) +-

    test.. test... test..... test?..... test!....

    !!!!!! ???? ,,  -- ---

    "Smartypants, double quotes" and 'single quotes'


    ## Emphasis

    **This is bold text**

    __This is bold text__

    *This is italic text*

    _This is italic text_

    ~~Strikethrough~~


    ## Blockquotes


    > Blockquotes can also be nested...
    >> ...by using additional greater-than signs right next to each other...
    > > > ...or with spaces between arrows.


    ## Lists

    Unordered

    + Create a list by starting a line with `+`, `-`, or `*`
    + Sub-lists are made by indenting 2 spaces:
    - Marker character change forces new list start:
        * Ac tristique libero volutpat at
        + Facilisis in pretium nisl aliquet
        - Nulla volutpat aliquam velit
    + Very easy!

    Ordered

    1. Lorem ipsum dolor sit amet
    2. Consectetur adipiscing elit
    3. Integer molestie lorem at massa


    1. You can use sequential numbers...
    1. ...or keep all the numbers as `1.`

    Start numbering with offset:

    57. foo
    1. bar


    ## Code

    Inline `code`

    Indented code

        // Some comments
        line 1 of code
        line 2 of code
        line 3 of code


    Block code "fences"

    ```
    Sample text here...
    ```

    Syntax highlighting

    ``` js
    var foo = function (bar) {
    return bar++;
    };

    console.log(foo(5));
    ```


Head over to your ``index.rst`` and add ``mymarkdown`` to the toctree.

.. code-block:: RST

    .. WFRT-DEMO documentation master file, created by
    sphinx-quickstart on Wed Sep 16 13:47:52 2020.
    You can adapt this file completely to your liking, but it should at least
    contain the root `toctree` directive.

    Welcome to WFRT-DEMO's documentation!
    =====================================

    .. toctree::
    :maxdepth: 2
    :caption: Contents:

       api
       mymarkdown

    Indices and tables
    ==================

    * :ref:`genindex`
    * :ref:`modindex`
    * :ref:`search`


Lets rebuild our webiste

.. code-block:: bash

    make clean
    make html

Push this work to `GitHub <github.com>`_ and see the new markdown page.

.. code-block:: bash

    git add .
    git commit -m "added mymarkdown to docs"
    git push
