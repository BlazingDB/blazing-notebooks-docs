.. _release_0_14:

============
Release 0.14
============

New Features
============
* New execution architecture, supporting executing queries on data that does not fit in the GPU. The new architecture features the following:
    * The execution model is an acyclic graph of execution nodes with a cache in between execution nodes. 
    * Each execution node operates independently on batches of data, allowing it to process steps in parallel as much as possible instead of sequentially. 
    * Each cache between every execution step can hold the data in GPU, in system memory or on disk.
    * Has support for multi-partition dask.cudf.DataFrame result set outputs.

* Added ability to set configuration options
* Added support for using NULL as a literal value
* Implemented `CHAR_LENGTH function <https://docs.blazingdb.com/v0.14/docs/string-functions#char_length>`_
* Added ability to specify region for S3 buckets
* Added type normalization for UNION ALL
* Added support for `MinIO Storage <https://docs.blazingdb.com/v0.14/docs/minio>`_

Improvements
============
* Improved support for CAST function to include TINYINT and SMALLINT
* Handle behavior when the optimized plan contains a LogicalValues
* Improvements to exception handling
* Support modern compilers (>= g++-7.x)
* Improved logging now uses spdlog
* Adding event logging
* BlazingSQL engine no longer needs to concatenate dask.cudf.DataFrame partitions prior to running a query on a dask.cudf.DataFrame table
* Improved expression parser, including support for expression trees of unlimited size.
* Optimized data loading for queries of the type: SELECT * FROM table LIMIT N
* Added built in end to end testing framework
* Added logging to condition variables that are waiting too long


Bug Fixes
=========
* Fixed bug in size estimation for tables before joins
* Fixed issue with excessive thread creation in communication
* Fixed bug in expression parsing for joins
* Fixed bug caused by sharing data loaders when a query has one table more than once
* Fixed Hive file format inference

.. toctree::
    :maxdepth: 2
    :hidden:

