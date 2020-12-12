.. _release_0_17:

============
Release 0.17
============

New SQL Functions
=================
The following SQL commands are now supported

* TO_DATE / TO_TIMESTAMP 
* DAYOFWEEK
* TRIM / LTRIM / RTRIM
* LEFT  / RIGHT 
* UPPER / LOWER
* REPLACE
* REVERSE

New Features
============
* **New communications architecture with support for both TCP and UCX (UCX support is in beta)**
* Allow to create tables from compressed text delimited files
* Allow to create tables off of Hive partitioned folder structure, where BlazingSQL will infer columns and types.
* Added powerPC building script and instructions
* Added local logging directory option to BlazingContext to help resolve logging file permission issues
* Added option to read csv files in chunks
* Logs are now configurable to have max size and be rotated

Improvements
============
* Added Apache Calcite rule for window functions. (Window functions not supported yet)
* Add validation for the kwargs when BlazingContext.create_table API is called
* Added validation for s3 buckets
* Added scheduler file support for e2e testing framework
* Improved how sampling is done for ORDER BY
* Several changes to keep up with cuDF API changes
* Remove temp files when an error occurs
* Added new end-to-end tests
* Added new unit tests
* Improved contribution documentation 
* Code refactoring and removing dead or duplicate code

Improvements in error logging 
=============================
* Improvement to error messaging when validating any GCP bucket
* Added error logging in DataSourceSequence
* Showing an appropriate error to indicate that we don't support opening directories with wildcards
* Showing an appropriate error for invalid or unsupported expressions on the logical plan

Changes or improvements in technology stack or CI
=================================================
* Added output compile json option for cppcheck
* Bump junit from 4.12 to 4.13.1 in /algebra
* Improved gpuCI scripts
* Removed need to specify cuda version via a label for conda packages
* Fixed cmake version to be 3.18.4
* Fix SSL errors for conda

Bug Fixes
=========
* Fixed issue when loading parquet files with local_files=True
* Fixed logging directory setup
* Fixed issues with config_options 
* Fixed issue in float columns when parsing parquet metadata
* Fixed bug in MergeAggregations when single node has multiple batches
* Fix graph thread pool hang when exception is thrown
* Fix ignore headers when multiple CSV files was provided
* Fix column_names (table) always as list of string
* Fixed literal type inference for integers

Deprecated features
===================
* Deprecated bc.partition

.. toctree::
    :maxdepth: 2
    :hidden:

