Docstrings
=============

There are several different docstring formats which one can use in order to enable Sphinx's ``autodoc`` 
extension to automatically generate documentation. For this tutorial we will use the ``Sphinx`` format, 
since, as the name suggests, it is the standard format used with Sphinx. Other formats include
`Google <https://sphinxcontrib-napoleon.readthedocs.io/en/latest/example_google.html>`_) and
`NumPy <http://sphinxcontrib-napoleon.readthedocs.io/en/latest/example_numpy.html#example-numpy>`_,
but they require the use of Sphinx's ``napoleon`` extension, which is beyond the scope of this tutorial.

NumPy Docstrings example for a function
--------------------------------------------

.. code-block:: python

    def function_with_types_in_docstring(param1, param2):
        """Example function with types documented in the docstring.

        `PEP 484`_ type annotations are supported. If attribute, parameter, and
        return types are annotated according to `PEP 484`_, they do not need to be
        included in the docstring:

        Parameters
        ----------
        param1 : int
            The first parameter.
        param2 : str
            The second parameter.

        Returns
        -------
        bool
            True if successful, False otherwise.

        .. _PEP 484:
            https://www.python.org/dev/peps/pep-0484/

        """

