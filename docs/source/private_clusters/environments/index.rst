.. _environments:

=====================
Managing environments
=====================

One of the most important parts of doing your work easy is making sure that you have a environment with
all all the packages that you need. BlazingSQL Notebooks app supports you managing your conda environments. You can create custom environments, 
but if you don't need any specific package you will have two default environments configurated to use rapids-stable or rapids-nightly 
and all the dependencies to try RAPIDS and BlazingSQL.  

Create an environment
=====================

Creating conda environments in BlazingSQL Notebooks is just about fullfill the form with the values for the required parameters.

.. raw:: html

    <img src="../../_static/images/create_custom_env.png" alt="create_custom_environment"/>


**Required parameters:**

**Name:** Should be something that is easy for you to identify your conda environment.

**Description:** This parameter is about some detail that you want to save for your environment.

**Packages:** In this field you have to specify the channels and dependencies that you want to have to installed in your conda environment. To make it easy, 
you will see a structure there when you go to the create custom environment form. 

**Example:**

:: 

    channels:
        - blazingsql/label/cuda10.2
        - rapidsai
        - nvidia
        - conda-forge
        - defaults
    dependencies:
        - blazingsql
        - python=3.8
        - dask
        - cudf
        - cudatoolkit=10.2

Base environments
=================

BlazingSQL Notebooks app allows users to create custom environments, but by default 
we provide you two base environments built with RAPIDS-stable and RAPIDS-nightly. Those environments can'tempor
be eddited and deleted. 

RAPIDS-stable
-------------

It is a base environment that include RAPIDS and BlazingSQL from stable channels.

::

    channels:
        - pytorch
        - plotly
        - blazingsql
        - rapidsai
        - nvidia
        - conda-forge
        - defaults
    dependencies:
        - blazingsql
        - python=3.8
        - dask
        - cuml
        - cuxfilter
        - clx
        - cugraph
        - cuspatial
        - cusignal
        - colorcet
        - datashader
        - fbprophet
        - geoviews
        - holoviews
        - pytorch=1.6
        - scikit-learn
        - networkx
        - scipy
        - dask-ml
        - matplotlib
        - statsmodels
        - xgboost
        - seaborn
        - ipywidgets
        - python-graphviz
        - cudatoolkit=10.2
        - spacy
        - s3fs=0.5.1
        - panel=0.9.7
        - plotly
        - dash
        - jupyter-dash
        - pip: 
            - graphistry==0.14.0


RAPIDS-nightly
--------------

It is a base environment that include RAPIDS and BlazingSQL from nightly channels.

::

    channels:
        - pytorch
        - plotly
        - blazingsql-nightly
        - rapidsai-nightly
        - nvidia
        - conda-forge
        - defaults
    dependencies:
        - blazingsql
        - python=3.8
        - dask
        - cuml
        - cuxfilter
        - clx
        - cugraph
        - cuspatial
        - cusignal
        - colorcet
        - datashader
        - fbprophet
        - geoviews
        - holoviews
        - pytorch=1.6
        - scikit-learn
        - networkx
        - scipy
        - dask-ml
        - matplotlib
        - statsmodels
        - xgboost
        - seaborn
        - ipywidgets
        - python-graphviz
        - cudatoolkit=10.2
        - spacy
        - s3fs=0.5.1
        - panel=0.9.7
        - plotly
        - dash
        - jupyter-dash
        - pip: 
            - graphistry==0.14.0


Delete an environment
=====================

To delete a custom conda environment,  you only have to do click on the *"Delete"* button.

Edit and update an environment
==============================

Lorem ipsum dolor sit amet, consectetur adipiscing elit, 
sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. 
Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris 
nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in 
reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla 
pariatur. Excepteur sint occaecat cupidatat non proident, sunt in 
culpa qui officia deserunt mollit anim id est laborum.

.. toctree::
    :maxdepth: 2