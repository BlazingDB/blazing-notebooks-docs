.. _environments:

=====================
Managing environments
=====================

One of the most important parts of doing your work easy is making sure that you have a environment with
all all the packages that you need. The Blazing Notebooks provides and easy way to managing your conda environments. 
You can create custom environments, but if you don't need any specific package you will have two default environments configured 
to use *rapids-stable* or *rapids-nightly* 
and all the dependencies to try RAPIDS and BlazingSQL;
see what is included in the **Base environments** section below.

Create an environment
=====================

To create conda environment in Blazing Notebooks just fill the form with the required parameters.

.. raw:: html

    <div class="col-lg-12 col-md-12 col-sm-12 col-xs-12 d-flex text-center image">
        <div class="shadow image text-center ">
            <img src="../../_static/images/create_custom_env.png" alt="create_custom_environment" width=400/>
        </div>
    </div>

|

**Required parameters:**

1. **Name:** A recognizable name for the environment.
2. **Description:** A short description of the environment.
3. **Packages:** List of channels and dependencies that will be installed in your conda environment. To get started, Blazing Notebooks pre-populates the structure. 

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

.. _base_envs:

Base environments
=================

Blazing Notebooks app allows users to create custom environments, but by default 
two base environments built with RAPIDS-stable and RAPIDS-nightly are provided. 
Those environments **cannot** be eddited and deleted. 

RAPIDS-stable
-------------

The base environment that includes RAPIDS and BlazingSQL packages from stable channels.

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

The base environment that includes RAPIDS and BlazingSQL packages from nightly channels.

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

To delete a custom conda environment click the *"Delete"* button.

.. raw:: html

    <div class="col-lg-12 col-md-12 col-sm-12 col-xs-12 d-flex text-center image">
        <div class="shadow image text-center ">
            <img src="../../_static/images/list_custom_env.png" alt="list_custom_environment" width=400/>
        </div>
    </div>

|

You will be asked to *confirm* or *cancel* the operation

.. raw:: html

    <div class="col-lg-12 col-md-12 col-sm-12 col-xs-12 d-flex text-center image">
        <div class="shadow image text-center ">
            <img src="../../_static/images/delete_environment.png" alt="list_custom_environment" width=300/>
        </div>
    </div>

|

If you confirm, the environment will be deleted.

Edit and update an environment
==============================

Environments are editable. To edit a custom conda environmet and change any of the parameters or packages that were included when the environment was created click
the **Edit** button and update the form.

.. raw:: html

    <div class="col-lg-12 col-md-12 col-sm-12 col-xs-12 d-flex text-center image">
        <div class="shadow image text-center ">
            <img src="../../_static/images/edit_custom_env.png" alt="list_custom_environment" width=600/>
        </div>
    </div>

.. toctree::
    :maxdepth: 2