.. _release_0_11:

============
Release 0.11
============

New Features
============
* Merged all the code repos for the whole stack into one repo
* Pythonization of the whole BlazingSQL stack. See our `blog post <https://blog.blazingdb.com/can-you-fit-a-distributed-sql-engine-into-a-python-package-2216479bf14c>`_ for more information
* New API for being able to query performance and execution `logs <https://docs.blazingdb.com/docs/blazingsql-logs>`_
* Ability to create BlazingSQL tables from `Hive tables <https://docs.blazingdb.com/docs/hive>`_
* Partial support for Non-equality joins. For example  SELECT * FROM tableA as A INNER JOIN tableB as B ON A.key = B.key AND A.this_date > B.that_date
* Added arrow-provider

Improvements
============
* Optimized simple queries that only have COUNT(*)
* Removed limitation on number of operands for outer joins
* Improved error messaging
* Improvements to relational algebra optimization

Bug Fixes
=========
* Fixed bug where a python script running BlazingSQL would hang at the end of a script
* Fixed bug when using wildcards for file paths and using dask distribution
* Fixed bug with HDFS
* Fixed bug with projects with large amounts of transformations on large GPUs
* Fixed bug with multiple projections on the same column
* Fixed COUNT(*) to properly ignore nulls
* Fixed stability issues with certains queries running on 3 or more nodes
* Fixed bug with querying a GDF and no transformations are applied
* Fixed bug with empty result sets
* Fixed bug with empty column names

.. toctree::
    :maxdepth: 2
    :hidden:

