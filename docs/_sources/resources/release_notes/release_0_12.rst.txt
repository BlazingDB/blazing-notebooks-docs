.. _release_0_12:

============
Release 0.12
============

New Features
============
* Ability to skip reading and processing row groups when querying Apache Parquet files by applying predicates on metadata
* Ability to do SELECT COUNT (DISTINCT column)
* Ability to use and set Pool memory allocator for increased performance and/or managed (UVM) allocator which provides robustness against running out of GPU memory

Improvements
============
* New building scripts thanks to @dillon-cullinan

Bug Fixes
=========
* Fixed various bugs in the Apache Arrow provider
* Fixed bug with incorrect data type in CASE statements
* Fixed bug and memory leak in distributed joins
* Fixed bug in usage of Google Cloud Storage plugin

.. toctree::
    :maxdepth: 2
    :hidden:

