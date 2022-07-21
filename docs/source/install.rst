Installation
==============

Lets install `Sphinx! <https://www.sphinx-doc.org/en/master/usage/installation.html>`_


You can install sphinx with either conda or pip.

.. note::
    If you are using conda (which I recommend) I have added a file called ``wfrt.yml``
    You can simply run the following command which will install a conda environment containing all the required packages for this user guide.

.. code-block:: bash

    conda env create -f wfrt.yml


Conda
++++++

If you dont want a new conda env

.. code-block:: bash

    conda install -c conda-forge sphinx
    conda install jupytext -c conda-forge
    conda install -c conda-forge nbsphinx
    conda install -c conda-forge myst-parser
    conda install -c conda-forge sphinx-book-theme
    conda install -c conda-forge sphinx-copybutton




Pip
++++++

Or if you like pip

.. code-block:: bash

    pip install sphinx
    pip install jupytext
    pip install nbsphinx
    pip install myst-parser
    pip install sphinx-book-theme
    pip install sphinx-copybutton
