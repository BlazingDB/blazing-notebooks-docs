.. _notebooks:

=========
Notebooks
=========

Working with notebooks
======================

Lorem ipsum dolor sit amet, consectetur adipiscing elit, 
sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. 
Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris 
nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in 
reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla 
pariatur. Excepteur sint occaecat cupidatat non proident, sunt in 
culpa qui officia deserunt mollit anim id est laborum.

Create notebooks
================

Creating a new notebook is really easy. You only have to click on the button of 
"Notebook section".

.. raw:: html

    <img src="../../_static/images/create_notebook.png" alt="jupyter_window" width=700/>

|

Then, you will see you something like this:

.. raw:: html

    <img src="../../_static/images/new_notebook.png" alt="jupyter_window" width=700/>


Open notebooks
==============

To open an existing notebook, you should go to the file list on the left side of the window 
and double-click on the notebook you want to open and you will see your notebook in the 
rigth side of the window.

.. raw:: html

    <img src="../../_static/images/open_notebook.png" alt="jupyter_window" width=700/>


Run notebooks
=============

Lorem ipsum dolor sit amet, consectetur adipiscing elit, 
sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. 
Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris 
nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in 
reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla 
pariatur. Excepteur sint occaecat cupidatat non proident, sunt in 
culpa qui officia deserunt mollit anim id est laborum.

Using Markdown
====================================

A Markdown cell contains text formatted using Markdown and displays 
its output in-place when the Markdown cell is run. 
To use Markdown you should click on the cell that you want to format
and go to *"Markdown"* option. Then the current cell will be ready to format
the text.

.. raw:: html

    <img src="../../_static/images/markdown.png" alt="jupyter_window" width=700/>

|

To make text italic or bold by surrounding a block of text with a single or double * respectively.

As headings by starting a line with one (or multiple) # followed by a space, as in the following example:

**Example:**

::

    # Heading 1
    # Heading 2
    ## Heading 2.1
    ## Heading 2.2

You can also use Markdown to create lists using the following syntax:

::

    * This is a bullet list
    * This is a bullet list
    * This is a bullet list


    1. And you can also create ordered lists
    2. by using numbers
    3. and listing new items in the lists 
    4. on their own lines

|

.. raw:: html

    <img src="../../_static/images/markdown_example.png" alt="jupyter_window" width=700/>


Jupyter Lab magics
==================

Lorem ipsum dolor sit amet, consectetur adipiscing elit, 
sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. 
Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris 
nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in 
reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla 
pariatur. Excepteur sint occaecat cupidatat non proident, sunt in 
culpa qui officia deserunt mollit anim id est laborum.

Using Blazing SQL/RAPIDS
========================

When you create a private cluster in BlazingSQL Notebooks app, you 
are ready to start using BlazingSQL and RAPIDS. 
You only have to import blazingsql and start creating tables and 
running queries.

::

    from blazingsql import BlazingContext

    bc = BlazingContext()

    bc.create_table('table_name_01', 'dir_file') 

    query = ''' 
        SELECT * FROM table_name_01
        '''

    gdf = bc.sql(query)


Register external data sources with BlazingContext
==================================================

BlazingSQL Filesystem API allow users register and connect 
to S3 storage. BlazingSQL can query any supported file format 
on a registered filesystem, which typically optimizes the reading 
of data during query execution.

Once a filesystem is registered you can reference the user-defined 
file path when creating a new table off of a file.

S3 
--

After you create your notebook, you will register an S3 bucket to a BlazingContext. The context 
will maintain the information necessary for BlazingSQL to query 
data stored in the S3 bucket.

::

    from blazingsql import BlazingContext
    bc = BlazingContext() 

::

    bc.s3('dir_name', 
        bucket_name='bucket_name', 
        access_key_id='access_key', 
        secret_key='secret_key')

FileBase
--------

BlazingSQL logs
===============

BlazingSQL has an internal log that records events including runtime query step 
execution information, performance timings, errors and warnings. 
The logs table is called bsql_logs. You can query the logs as if 
it were any other table using log function of Blazing Context.

::

    from blazingsql import BlazingContext
    bc = BlazingContext()

    # query how long each query took
    log_result = bc.log("SELECT log_time, query_id, duration FROM bsql_logs WHERE info = 'Query Execution Done' ORDER BY log_time DESC")
    print(log_result)

Delete notebooks
================

To delete a notebook from JupyterLab, you can go yo the *"Terminal"* and execute ``rm filename.ipynb``.

.. raw:: html

    <img src="../../_static/images/delete_notebooks.png" alt="delete_notebooks" width=700/>

.. toctree::
    :maxdepth: 3