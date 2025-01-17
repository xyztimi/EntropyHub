  .. currentmodule:: EntropyHub


=======================
Bidimensional Entropies
=======================

.. toctree::
   :maxdepth: 3


Functions for estimating the entropy of a two-dimensional univariate matrix.
****************************************************************************

While EntropyHub functions primarily apply to time series data, with the following
bidimensional entropy functions one can estimate the entropy of two-dimensional (2D)
matrices. Hence, bidimensional entropy functions are useful for applications such as image/texture analysis.

.. danger:: 
    
    ``IMPORTANT: Locked Matrix Size``

    Each bidimensional entropy function (``SampEn2D``, ``FuzzEn2D``, ``DistEn2D``, ``DispEn2D``, ``PermEn2D``, ``EspEn2D``) has
    an important keyword argument - ``Lock``. Bidimensional entropy functions are
    "locked" by default (``Lock == true``) to only permit matrices with a maximum size of 128 x 128.

    The reason for this is because there are hundreds of millions of pairwise calculations
    performed in the estimation of bidimensional entropy, so memory errors often
    occur when storing data on RAM.

    e.g. For a matrix of size [200 x 200], an embedding dimension (``m``) = 3, and a time
    delay (``tau``) = 1, there are 753,049,836 pairwise matrix comparisons (6,777,448,524
    elemental subtractions).
    To pass matrices with sizes greater than [128 x 128], set `Lock = false`.

    ``CAUTION: unlocking the permitted matrix size may cause your MatLab application to crash.``

    

.................................................................................................


.. mat:automodule:: EntropyHub
   :members: SampEn2D, FuzzEn2D, DistEn2D, DispEn2D, PermEn2D, EspEn2D

