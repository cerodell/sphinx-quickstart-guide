Docstrings
=============

To use Sphinx to auto-document your code you need to follow certain docstring formats within your code.
There are many options and for this tutorial, we will use the
`NumPy <http://sphinxcontrib-napoleon.readthedocs.io/en/latest/example_numpy.html#example-numpy>`_, format. 
Other formats include `Google <https://sphinxcontrib-napoleon.readthedocs.io/en/latest/example_google.html>`_
and `Sphinx <https://sphinx-rtd-tutorial.readthedocs.io/en/latest/docstrings.html>`_, docstrings.


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

