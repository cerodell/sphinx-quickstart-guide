Index / Toctree
======================

Now understanding the different ways to document python code lets bring some into our documentation webpage.

To do this we needed first need understand ``index.rst`` and ``toctree``


Here is our current ``index.rst``

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



    Indices and tables
    ==================

    * :ref:`genindex`
    * :ref:`modindex`
    * :ref:`search`


Ok, cool now how do we add to this? Let's find out!


Add to toctree
----------------

Lets make a new ``rst`` file called ``api.rst`` within our ``soure/`` folder

.. code-block:: bash

    touch api.rst

Lets leave ``api.rst`` blank for now and place it within the toctree

.. warning::
    When you add ``api`` to the toc-tree...ITS THREE SPACES IN FROM THE LEFT...not a tab or four or two spaces. Its very particular about that. Also you do NOT include the file extension.

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
   

    Indices and tables
    ==================

    * :ref:`genindex`
    * :ref:`modindex`
    * :ref:`search`

We will now add some code to our webpage!