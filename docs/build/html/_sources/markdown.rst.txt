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

.. code-block::  

    # Governing Equations

    The governing equations from Thomas Warner's book: Numerical Weather and Climate Prediction


    $$ \frac{\partial u}{\partial t}=-u \frac{\partial u}{\partial x}-v \frac{\partial u}{\partial y}-w \frac{\partial u}{\partial z}+\frac{u v \tan \phi}{a}-\frac{u w}{a}-\frac{1}{\rho} \frac{\partial p}{\partial x}-2 \Omega(w \cos \phi-v \sin \phi)+F r_{x} $$ (2.1)


    $$ \frac{\partial v}{\partial t}=-u \frac{\partial v}{\partial x}-v \frac{\partial v}{\partial y}-w \frac{\partial v}{\partial z}-\frac{u^{2} \tan \phi}{a}-\frac{u w}{a}-\frac{1}{\rho} \frac{\partial p}{\partial y}-2 \Omega u \sin \phi+F r_{y} $$ (2.2)


    $$ \frac{\partial w}{\partial t}=-u \frac{\partial w}{\partial x}-v \frac{\partial w}{\partial y}-w \frac{\partial w}{\partial z}-\frac{u^{2}+v^{2}}{a}-\frac{1}{\rho} \frac{\partial p}{\partial z}+2 \Omega u \cos \phi-g+F r_{z} $$ (2.3)


    $$ \frac{\partial T}{\partial t}=-u \frac{\partial T}{\partial x}-v \frac{\partial T}{\partial y}+\left(\gamma-\gamma_{d}\right) w+\frac{1}{c_{p}} \frac{d H}{d t} $$ (2.4)


    $$ \frac{\partial \rho}{\partial t}=-u \frac{\partial \rho}{\partial x}-v \frac{\partial \rho}{\partial y}-w \frac{\partial \rho}{\partial z}-\rho\left(\frac{\partial u}{\partial x}+\frac{\partial v}{\partial y}+\frac{\partial w}{\partial z}\right) $$ (2.5)


    $$ \frac{\partial q_{v}}{\partial t}=-u \frac{\partial q_{v}}{\partial x}-v \frac{\partial q_{v}}{\partial y}-w \frac{\partial q_{v}}{\partial z}+Q_{v} $$ (2.6)


    $$ P=\rho R T $$ (2.7)


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


Push this work to `GitHub <github.com>`_ and see the new markdown page.

.. code-block:: bash 

    git add .
    git commit -m "added mymarkdown to docs"
    git push