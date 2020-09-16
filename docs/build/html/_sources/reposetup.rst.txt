
Repo Setup 
=============

In your porjects repository make a folder called ``docs`` 

.. code-block:: bash 

    cd /path/to/project
    mkdir docs

Now head into the ``docs/`` folder

.. code-block:: bash

    cd docs/

We are now going to run ``sphinx-quickstart`` inside the ``docs`` folder.
    * This will ask you a few questions

        #. Either, you use a directory ``_build`` within the root path, or you separate ``source`` and ``build`` directories within the root path.
        #. Project name:
        #. Author name(s):
        #. Project release []:
        #. Project language [en]:


.. important::
    Please answer yes to the first question by typing ``y`` than enter. You must say yes to this question for the rest of this quick start guide to function correctly. Answer the remaining questions however you would like. 


Lets run ``sphinx-quickstart`` by:

.. code-block:: bash 

   sphinx-quickstart


Here is an exmaple code block of each question youll be asked:

.. code-block:: bash 

    Welcome to the Sphinx 3.2.1 quickstart utility.

    Please enter values for the following settings (just press Enter to
    accept a default value, if one is given in brackets).

    Selected root path: .

    You have two options for placing the build directory for Sphinx output.
    Either, you use a directory "_build" within the root path, or you separate
    "source" and "build" directories within the root path.
    > Separate source and build directories (y/n) [n]: y

    The project name will occur in several places in the built documentation.
    > Project name: Sphinx Quickstart Guide
    > Author name(s): Christopher Rodell
    > Project release []: 

    If the documents are to be written in a language other than English,
    you can select a language here by its language code. Sphinx will then
    translate text that it generates into that language.

    For a list of supported codes, see
    https://www.sphinx-doc.org/en/master/usage/configuration.html#confval-language.
    > Project language [en]: 

    Creating file /Users/rodell/test/docs/source/conf.py.
    Creating file /Users/rodell/test/docs/source/index.rst.
    Creating file /Users/rodell/test/docs/Makefile.
    Creating file /Users/rodell/test/docs/make.bat.

    Finished: An initial directory structure has been created.

    You should now populate your master file /Users/rodell/test/docs/source/index.rst and create other documentation
    source files. Use the Makefile to build the docs, like so:
    make builder
    where "builder" is one of the supported builders, e.g. html, latex or linkcheck.

This is what your docs folder will look like if you followed the instruction above.

.. code-block:: bash

    docs
    ├── Makefile
    ├── build
    ├── make.bat
    └── source
        ├── _static
        ├── _templates
        ├── conf.py
        └── index.rst

We will now see a  some files along with a ``source`` and ``build`` folder

    * The ``source`` folder is the source directory that sphinx uses to build your website.

        - This is where you will be working most of the time
        - ``conf.py`` is the configuration script sphinx uses to build the website. We will discuss this in detail later
        - ``index.rst`` is the master document to serve as a welcome page, and the root of the website. We will also, discuss this in detail later

    * The ``build`` folder is the directory where sphinx will place your website's content.

        - You dont go here


Sneaky Tricks 
---------------

Now we will do two sneaky (yet simple) tricks to make your life much easier. 

In the ``docs/`` directory add the following two files. 

First, we will add a ``.nojekyll`` file to the docs directory  


    * This is an empty file and I dont fully understand what it does other than it make things work! 
    * If you want to learn what it does go here `<https://github.com/vercel/next.js/issues/2029>`_ 

.. code-block:: bash

    touch .nojekyll
    
Second let's add an index.html file that contains a simple meta tag
 * The meta tage will redirect GitHub Pages to your build folder where your websites main index.html lives.
 * I like doing this as you can keep everything within your soruce folder. 

.. code-block:: bash

    touch index.html

copy the following meta tag 

.. code-block:: html

    <meta http-equiv="refresh" content="0; url=./build/html/index.html" />

and past into index.html

.. code-block:: bash

    vi index.html
    ## past meta tage and save
    
Horray we are making head way! Lets build a website!!!