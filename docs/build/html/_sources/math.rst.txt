Math Equations
==================

Adding math to your website is very easy in rst. You can use `LateX <https://www.latex-project.org/>`_ formate for math equations

In rst, all you need to do is:

.. code-block:: RST

    .. math::

        f(x)=\int_{0}^{x} f^{\prime}(t) d t



Example Equations
++++++++++++++++++++++++

The governing equations from Thomas Warner's book: Numerical Weather and Climate Prediction


.. math::

    \frac{\partial u}{\partial t}=-u \frac{\partial u}{\partial x}-v \frac{\partial u}{\partial y}-w \frac{\partial u}{\partial z}+\frac{u v \tan \phi}{a}-\frac{u w}{a}-\frac{1}{\rho} \frac{\partial p}{\partial x}-2 \Omega(w \cos \phi-v \sin \phi)+F r_{x}

    \\

    \frac{\partial v}{\partial t}=-u \frac{\partial v}{\partial x}-v \frac{\partial v}{\partial y}-w \frac{\partial v}{\partial z}-\frac{u^{2} \tan \phi}{a}-\frac{u w}{a}-\frac{1}{\rho} \frac{\partial p}{\partial y}-2 \Omega u \sin \phi+F r_{y}

    \\

    \frac{\partial w}{\partial t}=-u \frac{\partial w}{\partial x}-v \frac{\partial w}{\partial y}-w \frac{\partial w}{\partial z}-\frac{u^{2}+v^{2}}{a}-\frac{1}{\rho} \frac{\partial p}{\partial z}+2 \Omega u \cos \phi-g+F r_{z}

    \\

    \frac{\partial T}{\partial t}=-u \frac{\partial T}{\partial x}-v \frac{\partial T}{\partial y}+\left(\gamma-\gamma_{d}\right) w+\frac{1}{c_{p}} \frac{d H}{d t}

    \\

    \frac{\partial \rho}{\partial t}=-u \frac{\partial \rho}{\partial x}-v \frac{\partial \rho}{\partial y}-w \frac{\partial \rho}{\partial z}-\rho\left(\frac{\partial u}{\partial x}+\frac{\partial v}{\partial y}+\frac{\partial w}{\partial z}\right)

    \\

    \frac{\partial q_{v}}{\partial t}=-u \frac{\partial q_{v}}{\partial x}-v \frac{\partial q_{v}}{\partial y}-w \frac{\partial q_{v}}{\partial z}+Q_{v}

    \\

    P=\rho R T


Math in Markdown
++++++++++++++++++++++++

In the ``source/`` folder make a file call ``mathmd.md``

.. code-block:: bash

    touch mathmd.md

Open ``mathmd.md`` and add the flowing latex example

.. code-block::

    $$
    \frac{\partial u}{\partial t}=-u \frac{\partial u}{\partial x}-v \frac{\partial u}{\partial y}-w \frac{\partial u}{\partial z}+\frac{u v \tan \phi}{a}-\frac{u w}{a}-\frac{1}{\rho} \frac{\partial p}{\partial x}-2 \Omega(w \cos \phi-v \sin \phi)+F r_{x}
    $$

    <br>

    $$
    \frac{\partial v}{\partial t}=-u \frac{\partial v}{\partial x}-v \frac{\partial v}{\partial y}-w \frac{\partial v}{\partial z}-\frac{u^{2} \tan \phi}{a}-\frac{u w}{a}-\frac{1}{\rho} \frac{\partial p}{\partial y}-2 \Omega u \sin \phi+F r_{y}
    $$

    <br>

    $$
    \frac{\partial w}{\partial t}=-u \frac{\partial w}{\partial x}-v \frac{\partial w}{\partial y}-w \frac{\partial w}{\partial z}-\frac{u^{2}+v^{2}}{a}-\frac{1}{\rho} \frac{\partial p}{\partial z}+2 \Omega u \cos \phi-g+F r_{z}
    $$

    <br>

    $$
    \frac{\partial T}{\partial t}=-u \frac{\partial T}{\partial x}-v \frac{\partial T}{\partial y}+\left(\gamma-\gamma_{d}\right) w+\frac{1}{c_{p}} \frac{d H}{d t}
    $$

    <br>

    $$
    \frac{\partial \rho}{\partial t}=-u \frac{\partial \rho}{\partial x}-v \frac{\partial \rho}{\partial y}-w \frac{\partial \rho}{\partial z}-\rho\left(\frac{\partial u}{\partial x}+\frac{\partial v}{\partial y}+\frac{\partial w}{\partial z}\right)
    $$

    <br>

    $$
    \frac{\partial q_{v}}{\partial t}=-u \frac{\partial q_{v}}{\partial x}-v \frac{\partial q_{v}}{\partial y}-w \frac{\partial q_{v}}{\partial z}+Q_{v}
    $$

    <br>

    $$
    P=\rho R T
    $$

Head over to your ``index.rst`` and add ``mathmd`` to the toctree.

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
       mathmd

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
    git commit -m "added mathmd to docs"
    git push
