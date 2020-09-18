Math Equations
==================

Adding math to your website is very easy in rst. You can use `LateX <https://www.latex-project.org/>`_ formate for math equations

All you need to do is:

.. code-block:: RST

    .. math::

        f(x)=\int_{0}^{x} f^{\prime}(t) d t




Example Equations
++++++++++++++++++++++++

The governing equations from Thomas Warner's book: Numerical Weather and Climate Prediction


.. math::

    \frac{\partial u}{\partial t}=-u \frac{\partial u}{\partial x}-v \frac{\partial u}{\partial y}-w \frac{\partial u}{\partial z}+\frac{u v \tan \phi}{a}-\frac{u w}{a}-\frac{1}{\rho} \frac{\partial p}{\partial x}-2 \Omega(w \cos \phi-v \sin \phi)+F r_{x}  (2.1)

    \\

    \frac{\partial v}{\partial t}=-u \frac{\partial v}{\partial x}-v \frac{\partial v}{\partial y}-w \frac{\partial v}{\partial z}-\frac{u^{2} \tan \phi}{a}-\frac{u w}{a}-\frac{1}{\rho} \frac{\partial p}{\partial y}-2 \Omega u \sin \phi+F r_{y}  (2.2)

    \\

    \frac{\partial w}{\partial t}=-u \frac{\partial w}{\partial x}-v \frac{\partial w}{\partial y}-w \frac{\partial w}{\partial z}-\frac{u^{2}+v^{2}}{a}-\frac{1}{\rho} \frac{\partial p}{\partial z}+2 \Omega u \cos \phi-g+F r_{z}  (2.3)

    \\

    \frac{\partial T}{\partial t}=-u \frac{\partial T}{\partial x}-v \frac{\partial T}{\partial y}+\left(\gamma-\gamma_{d}\right) w+\frac{1}{c_{p}} \frac{d H}{d t}  (2.4)

    \\

    \frac{\partial \rho}{\partial t}=-u \frac{\partial \rho}{\partial x}-v \frac{\partial \rho}{\partial y}-w \frac{\partial \rho}{\partial z}-\rho\left(\frac{\partial u}{\partial x}+\frac{\partial v}{\partial y}+\frac{\partial w}{\partial z}\right)  (2.5)

    \\

    \frac{\partial q_{v}}{\partial t}=-u \frac{\partial q_{v}}{\partial x}-v \frac{\partial q_{v}}{\partial y}-w \frac{\partial q_{v}}{\partial z}+Q_{v}  (2.6)

    \\
    
    P=\rho R T  (2.7)