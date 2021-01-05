.. _release_0_13:

============
Release 0.13
============

New Features
============
* Support for AVG in distributed mode
* Added ability to use existing memory allocator
* Implemented `unify_partitions <https://docs.blazingdb.com/docs/unify_partitions>`_ function for preparing dask_cudf DataFrames prior to creating BlazingSQL tables
* Implemented ROUND function
* Implemented support for CASE with strings

Improvements
============
* Local files can be referenced with relative file paths when creating tables.
* Automatic casting for joins on similar data types (i.e. joining an int32 with an int64 will cast the int32 to an int64)
* Updated AWS SDK version
* More changes to related to changes migration of libcudf to libcudf++
* Added docstrings to main python APIs

Bug Fixes
=========
* Fixed bug when for joining against empty DataFrame
* Fixed bug with GROUP BY ignoring nulls
* Fixed various issues related to creating tables from dask_cudf DataFrames
* Fixed various bugs with creating tables from Hive Cursor
* Fixed bugs related to new libcudf++ functionality
* Fixed bug in LIMIT statement
* Fixed bug in timestamp processing
* Fixed bug in SUM0 aggregation (which enables COUNT DISTINCT)
* Fixed bug when querying single file with multiple workers
* Fixed bug with distributed COUNT aggregation without GROUP BY
* Fixed bug when creating and querying a table with several Apache Parquet files and one is empty
* Fixed bug with joins with nulls in the join key columns

Other
=====
* Temporarily deprecated JSON reader. In the meantime we recommend using: :code:`cudf.read_json`

.. toctree::
    :maxdepth: 2
    :hidden:

