======
Series
======
.. currentmodule:: cudf

Constructor
-----------
.. autosummary::
   :toctree: api/
   :template: autosummary/class_with_autosummary.rst

   Series

Attributes
----------
**Axes**

.. autosummary::
   :toctree: api/

   Series.index
   Series.values
   Series.data
   Series.dtype
   Series.shape
   Series.ndim
   Series.nullable
   Series.nullmask
   Series.null_count
   Series.size
   Series.memory_usage
   Series.has_nulls
   Series.empty
   Series.name
   Series.valid_count
   Series.values_host

Conversion
----------
.. autosummary::
   :toctree: api/

   Series.astype
   Series.copy
   Series.to_list
   Series.__array__
   Series.as_index
   Series.as_mask
   Series.scale


Indexing, iteration
-------------------
.. autosummary::
   :toctree: api/

   Series.loc
   Series.iloc
   Series.__iter__
   Series.items
   Series.iteritems
   Series.keys

For more information on ``.at``, ``.iat``, ``.loc``, and
``.iloc``,  see the :ref:`indexing documentation <indexing>`.

Binary operator functions
-------------------------
.. autosummary::
   :toctree: api/

   Series.add
   Series.sub
   Series.subtract
   Series.mul
   Series.multiply
   Series.truediv
   Series.floordiv
   Series.mod
   Series.pow
   Series.radd
   Series.rsub
   Series.rmul
   Series.rtruediv
   Series.rfloordiv
   Series.rmod
   Series.rpow
   Series.round
   Series.lt
   Series.gt
   Series.le
   Series.ge
   Series.ne
   Series.eq
   Series.product

Function application, GroupBy & window
--------------------------------------
.. autosummary::
   :toctree: api/

   Series.applymap
   Series.map
   Series.groupby
   Series.rolling
   Series.pipe

.. _api.series.stats:

Computations / descriptive stats
--------------------------------
.. autosummary::
   :toctree: api/

   Series.abs
   Series.all
   Series.any
   Series.ceil
   Series.clip
   Series.corr
   Series.count
   Series.cov
   Series.cummax
   Series.cummin
   Series.cumprod
   Series.cumsum
   Series.describe
   Series.diff
   Series.digitize
   Series.factorize
   Series.floor
   Series.kurt
   Series.max
   Series.mean
   Series.median
   Series.min
   Series.mode
   Series.nlargest
   Series.nsmallest
   Series.prod
   Series.quantile
   Series.rank
   Series.skew
   Series.std
   Series.sum
   Series.var
   Series.kurtosis
   Series.unique
   Series.nunique
   Series.is_unique
   Series.is_monotonic
   Series.is_monotonic_increasing
   Series.is_monotonic_decreasing
   Series.value_counts

Reindexing / selection / label manipulation
-------------------------------------------
.. autosummary::
   :toctree: api/

   Series.drop
   Series.drop_duplicates
   Series.equals
   Series.head
   Series.isin
   Series.reindex
   Series.rename
   Series.reset_index
   Series.reverse
   Series.sample
   Series.set_index
   Series.set_mask
   Series.take
   Series.tail
   Series.tile
   Series.where
   Series.mask

Missing data handling
---------------------
.. autosummary::
   :toctree: api/

   Series.dropna
   Series.fillna
   Series.isna
   Series.isnull
   Series.nans_to_nulls
   Series.notna
   Series.notnull
   Series.replace

Reshaping, sorting
------------------
.. autosummary::
   :toctree: api/

   Series.argsort
   Series.interleave_columns
   Series.sort_values
   Series.sort_index
   Series.explode
   Series.scatter_by_map
   Series.searchsorted
   Series.repeat

Combining / comparing / joining / merging / encoding
----------------------------------------------------
.. autosummary::
   :toctree: api/

   Series.append
   Series.update
   Series.label_encoding
   Series.one_hot_encoding

Numerical operations
~~~~~~~~~~~~~~~~~~~~
.. autosummary::
   :toctree: api/

   Series.acos
   Series.asin
   Series.atan
   Series.cos
   Series.exp
   Series.log
   Series.sin
   Series.sqrt
   Series.tan

Time Series-related
-------------------
.. autosummary::
   :toctree: api/

   Series.shift

Accessors
---------

pandas provides dtype-specific methods under various accessors.
These are separate namespaces within :class:`Series` that only apply
to specific data types.

=========================== =================================
Data Type                   Accessor
=========================== =================================
Datetime, Timedelta         :ref:`dt <api.series.dt>`
String                      :ref:`str <api.series.str>`
Categorical                 :ref:`cat <api.series.cat>`
List                        :ref:`list <api.series.list>`
=========================== =================================

.. _api.series.dt:

Datetimelike properties
~~~~~~~~~~~~~~~~~~~~~~~

``Series.dt`` can be used to access the values of the series as
datetimelike and return several properties.
These can be accessed like ``Series.dt.<property>``.

Datetime properties
^^^^^^^^^^^^^^^^^^^
.. currentmodule:: cudf.core.series.DatetimeProperties

.. autosummary::
   :toctree: api/

   day
   dayofweek
   hour
   minute
   month
   second
   weekday
   year

Datetime methods
^^^^^^^^^^^^^^^^

.. autosummary::
   :toctree: api/

   strftime


Timedelta properties
^^^^^^^^^^^^^^^^^^^^

.. currentmodule:: cudf.core.series.TimedeltaProperties
.. autosummary::
   :toctree: api/

   components
   days
   microseconds
   nanoseconds
   seconds


.. _api.series.str:

String handling
~~~~~~~~~~~~~~~

``Series.str`` can be used to access the values of the series as
strings and apply several methods to it. These can be accessed like
``Series.str.<function/property>``.

.. currentmodule:: cudf.core.column.string.StringMethods
.. autosummary::
   :toctree: api/

   byte_count
   capitalize
   cat
   center
   character_ngrams
   character_tokenize
   code_points
   contains
   count
   detokenize
   edit_distance
   endswith
   extract
   filter_alphanum
   filter_characters
   filter_tokens
   find
   findall
   get
   get_json_object
   htoi
   index
   insert
   ip2int
   is_consonant
   is_vowel
   isalnum
   isalpha
   isdecimal
   isdigit
   isempty
   isfloat
   ishex
   isinteger
   isipv4
   isspace
   islower
   isnumeric
   isupper
   istimestamp
   join
   len
   ljust
   lower
   lstrip
   match
   ngrams
   ngrams_tokenize
   normalize_characters
   pad
   partition
   porter_stemmer_measure
   replace
   replace_tokens
   replace_with_backrefs
   rfind
   rindex
   rjust
   rpartition
   rstrip
   slice
   slice_from
   slice_replace
   split
   rsplit
   startswith
   strip
   subword_tokenize
   swapcase
   title
   token_count
   tokenize
   translate
   upper
   url_decode
   url_encode
   wrap
   zfill
   


..
    The following is needed to ensure the generated pages are created with the
    correct template (otherwise they would be created in the Series/Index class page)

..
    .. currentmodule:: cudf
    .. autosummary::
       :toctree: api/
       :template: autosummary/accessor.rst

       Series.str
       Series.cat
       Series.dt
       Index.str

.. _api.series.cat:

Categorical accessor
~~~~~~~~~~~~~~~~~~~~

Categorical-dtype specific methods and attributes are available under
the ``Series.cat`` accessor.

.. currentmodule:: cudf.core.column.categorical.CategoricalAccessor
.. autosummary::
   :toctree: api/

   categories
   ordered
   codes
   reorder_categories
   add_categories
   remove_categories
   set_categories
   as_ordered
   as_unordered


.. _api.series.list:

List handling
~~~~~~~~~~~~~

``Series.list`` can be used to access the values of the series as
lists and apply list methods to it. These can be accessed like
``Series.list.<function/property>``.

.. currentmodule:: cudf.core.column.lists.ListMethods
.. autosummary::
   :toctree: api/

   concat
   contains
   get
   len
   sort_values
   take
   unique


Serialization / IO / conversion
-------------------------------
.. currentmodule:: cudf
.. autosummary::
   :toctree: api/

   Series.to_array
   Series.to_arrow
   Series.to_dlpack
   Series.to_frame
   Series.to_gpu_array
   Series.to_hdf
   Series.to_json
   Series.to_pandas
   Series.to_string
   Series.from_arrow
   Series.from_categorical
   Series.from_masked_array
   Series.from_pandas
   Series.hash_encode
   Series.hash_values
   