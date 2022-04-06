Usage
=====

.. _installation:

Installation
------------

To use Lumache, first install it using pip:

.. code-block:: console

   (.venv) $ pip install lumache

Creating recipes
----------------

To retrieve a list of ``브러신`` ingredients, :py:func:`사기리`
you can use the ``lumache.get_random_ingredients()`` function:

.. autofunction:: lumache.get_random_ingredients

The ``kind`` parameter should be either ``"meat"``, ``"fish"``,
or ``"veggies"``. Otherwise, :py:func:`lumache.get_random_ingredients`
will raise an exception.

.. image:: https://github.com/lisney/kozilTuto/blob/main/docs/source/4g2.jpg?raw=true

.. image:: https://user-images.githubusercontent.com/30430227/138903925-8a367010-263c-4e17-bd28-a3f100db5058.png

>>> import 
['a','b']

.. autoexception:: lumache.InvalidKindError

For example:

>>> import lumache
>>> lumache.get_random_ingredients()
['shells', 'gorgonzola', 'parsley']

