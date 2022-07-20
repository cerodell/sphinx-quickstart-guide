Jupyter Notebook
==================



Now lets have some fun and add a Jupyter Notebook to our website

Install jupytext
---------------------

First, lets install `jupytext <https://jupytext.readthedocs.io/en/latest/install.html>`_


This will allows us to make ``.ipynb`` files from ``.py`` using the `percent format <https://jupytext.readthedocs.io/en/latest/formats.html#the-percent-format>`_

.. code-block:: bash

	conda install jupytext -c conda-forge

or

.. code-block:: bash

    pip install jupytext --upgrade


The percent format
--------------------

.. code-block:: python

  # %% [markdown]
  # This is a multiline
  # Markdown cell

  # %% [markdown]
  # Another Markdown cell


  # %%
  # This is a code cell
  class A():
      def one():
          return 1

      def two():
          return 2



Add a Notebook page to toctree
------------------------------------


In the ``source/`` folder make a file call ``mybook.py``

.. code-block:: bash

    touch mybook.py

Open ``mybook.py`` and copy past the Percent format example above to ``mybook.py``


Convert ``.py`` to ``.ipynb``
+++++++++++++++++++++++++++++++

In the terminal run the following command to convert ``.py`` to ``.ipynb``

.. code-block:: bash

  jupytext --to notebook mybook.py


Head back over to your ``index.rst`` and add ``mybook.ipynb`` to the toctree.

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
       mymath
       mybook

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
    git commit -m "added mybook to docs"
    git push
