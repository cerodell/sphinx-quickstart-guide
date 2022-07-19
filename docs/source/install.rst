Installation
==============

Lets install `Sphinx! <https://www.sphinx-doc.org/en/master/usage/installation.html>`_


You can install sphinx with either conda or pip.

.. note::
    If you are using conda (which I recommend) I have added a file called ``wfrt.yml``
    You can simply run the following command which will install a conda environment containing all the required packages for this user guide.

        * The wfrt env is a very stripped down env and I promise it won't be added clutter to your machine

.. code-block:: bash

    conda env create -f wfrt.yml


Conda
++++++

If you dont want a new conda env

.. code-block:: bash

    conda install -c conda-forge sphinx
    conda install -c conda-forge nbsphinx
    conda install -c conda-forge recommonmark
    conda install -c conda-forge sphinx-automodapi
    conda install -c conda-forge sphinx-book-theme
    conda install -c conda-forge sphinx-markdown-tables
    conda install -c conda-forge sphinx-autodoc-typehints






Pip
++++++

Or if you like pip

.. code-block:: bash

    pip install sphinx
    pip install nbsphinx
    pip install recommonmark
    pip install sphinx-automodapi
    pip install sphinx-book-theme
    pip install sphinx-markdown-tables
    pip install sphinx-autodoc-typehints
