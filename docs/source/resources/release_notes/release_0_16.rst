.. _release_0_16:

============
Release 0.16
============

Improvements
============

* Activate End-to-end test result validation for GPU_CI.
* Add capacity to set the transport memory
* Update conda recipe, remove cxx11 abi from cmake
* Just one initialize() function at beginning and add logs related to allocation stuff
* Make possible to read the system environment variables to setup config_option for BlazingContext
* Update TPCH queries for end to end tests: converting implicit joins into explicit joins
* Removing cudf source code dependency as some cudf utilities headers were exposed
* Can now set manually BLAZING_CACHE_DIRECTORY

Bug Fixes
=========

* Fixed issue due to cudf orc api change
* Fixed issue parsing fixed width string literals
* Fixed issue with hive string columns
* Fixed issue due to an rmm include
* Fixed build issues with latest rmm 0.16 and columnBasisTest due to deprecated drop_column() function
* Fix metadata mistmatch due to parsedMetadata, caused by parquet files that had only nulls in certain columns for only some files
* Removed workaround for parquet read schema
* Fixed issue caused by creating tables with multiple csv files and having BSQL infer the datatypes and having a dtypes mismatch
* Avoid read _metadata files
* Fixed issues with parsers, in particular ORC parser was misbehaving
* Fixed issue with logging directories in distributed environments
* Pinned google cloud version to 1.16
* Partial revert of some changes on parquet rowgroups flow with local_files=True
* Fixed issue when loading paths with wildcards
* Fixed issue with concat_all in concatenating cache
* Fix arrow and spdlog compilation issues
* Fixed intra-query memory leak in joins
* Fixed crash when loading an empty folder
* Fixed parseSchemaPython can throw exceptions

.. toctree::
    :maxdepth: 2
    :hidden: