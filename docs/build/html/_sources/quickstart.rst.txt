Quick Start
==============

This a quick guide showing you how:

#.  :ref:`How to Install Sphinx <Installation>`
#.  :ref:`Setting up your Repository <Repo Setup>`
#.  :ref:`Connect docs to GitHub Pages <Github Pages>`

Installation 
--------------

Lets `install Sphinx! <https://www.sphinx-doc.org/en/master/usage/installation.html>`_


I recommend using conda to install sphinx but pip works too. 

.. code-block:: bash 

    conda install -c conda-forge sphinx

    or

    pip install sphinx

Repo Setup 
--------------

Make a ``docs`` folder within your repo 

.. code-block:: bash 

    cd /path/to/project
    mkdir docs

Run ``sphinx-quickstart``:

.. code-block:: bash 

    cd docs
    sphinx-quickstart

Enter ``yes`` or ``y`` for the first question, and fill out ``project name`` and ``your name`` where appropriate.

The last question is asking to use English as the default language. I'll leave that for you to decide.

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

Sneaky Tricks 
+++++++++++++++

Now we will do two sneaky (yet simple) tricks to make your life much easier. 

First, we will add a ``.nojekyll`` file to the docs directory  

    * I dont fully understand what this does other than it make things work! 
    * If you want to learn what it does go here `<https://github.com/vercel/next.js/issues/2029>`_ 

.. code-block:: bash

    touch .nojekyll
    
Second lets add an index.html file that contian a simple meta tag
 * The meta tage will redirect your to diffenrt index.html in you build folder.
 * Doing this make life much easier as you can keep everything nice and clean with your soruce folder. 


First, lets update the `conf.py`
    * You can leave it as is but I am going to show you my preferred set up. 

.. code-block:: python 










We are now set up to build a website. Simply run:

.. code-block:: bash 

    make html

And we will have created our first wedpage. 

We will no see a ``source`` folder and ``build`` folder

As the names imply the `source` folder is the source directory that sphinx used to build your website. Sphinx places all built content within the `build` folder.

You'll be working in the `source` folder most of the time.
You will never really need to go into the `build` folder 


GitHub Pages
--------------


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

