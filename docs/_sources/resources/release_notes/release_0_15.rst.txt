.. _release_0_15:

============
Release 0.15
============

New Features
============
* Added a memory monitor for better memory management for out of core processing
* Added list_tables() and describe_table() functions
* Added support for constant expressions evaluation by Calcite
* Added support for cross join
* Added rand() and support for running unary operations on literals
* Added get_free_memory() function

Improvements
============

Performance improvements
------------------------
* Implemented Unordered pull from cache to help performance
* Concatenating cache improvement and replacing PartwiseJoin::load_set with a concatenating cache
* Adding max kernel num threads pool
* Added new separate thresh for concat cache

Stability improvements
----------------------
* Added checks for concatenation to prevent String overflow
* Added nogil statements for pure C functions in Cython
* Round robing dask workers on single gpu queries
* Reraising query errors in context.py
* Implemented using threadpool for outgoing messages

Documentation improvements
--------------------------
* Added exhale to generate doxygen for sphinx docs
* Added Sphinx based code architecture documentation
* Added doxygen comments to CacheMachine.h
* Added more documentation about memory management
* Updated readme
* Added doxygen comments to some kernels and the batch processing

Building improvements
---------------------
* Updated Calcite to the most recent version 1.23
* Added check for CUDF_HOME to allow build to use an existing prebuilt cudf source tree
* Python/Cython check code style
* Make AWS and GCS optional

Logging improvements
--------------------
* Logging level (flush_on) can be configurable
* Set log_level when using LOGGING_LEVEL param

Testing improvements
--------------------
* Added unit tests on Calcite to check how logical plans are affected when rulesets are updated
* Updated set of TPCH queries on the E2E tests
* Added initial set of unit tests for WaitingQueue and nullptr checks around spdlog calls
* Add unit test for Project kernel

Other improvements
------------------
* Removed a lot of dead code from the codebase
* Replace random_generator with cudf::sample
* Adding extern C for include files
* Use default client and network interface from Dask. BlazingSQL should now be able to infer the network interface.
* Updated the GPUManager functions
* Handle exceptions from pool_threads

Bug Fixes
=========

* Various fixing of issues due to updates to cudf
* Fixed issue with Hive partitions when doing SELECT *
* Normalize columns before distribution in JoinPartitionKernel
* Fixed issue with hive partitions base folder
* Fix interops operators output types
* Fix when the algebra plan was provided using one-line as logical plan
* Fix issue related to Hive metadata
* Remove temp files from data cached to disk
* Fix when checking only Limit and Scan Kernels
* Loading one file at a time (LimitKernel and ScanKernel)
* Fixed small issue with hive types conversion
* Fix for literal cast
* Fixed issue with start and length of substring being different types
* Fixed issue on logical plans when there is an EXISTS clause
* Fixed issue with casting string to string
* Fixed issue with getting table scan info
* Fixed row_groups issue in ParquetParser.cpp
* Fixed issue with some constant expressions not evaluated by calcite
* Fixed issue with log directory creation in a distributed environment
* Fixed issue where we were including testing hpp in our code
* Fixed optimization regression on the select count(*) case
* Fixed issue caused by using new arrow_io_source
* Fixed e2e string comparison
* Fixed random segfault issue in parser
* Fixed issue with column names on sample function
* Introduced config param for max orderby samples and fixed issue with oversampling in ORDER BY


.. toctree::
    :maxdepth: 2
    :hidden: