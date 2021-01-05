.. _freemium:

=================
Free GPU Instance
=================

The `Free GPU Instance <https://app.blazingsql.com>`_ is a private JupyterLab environment 
on shared GPU resources.

This is a perfect place to either get started with the 
RAPIDS ecosystem or prototype/build out workflows that you 
can launch at scale with the Private GPU Clusters.

The Free GPU Instance has two pre-configured RAPIDS environments:

- **RAPIDS Stable** - Updated every 6 weeks (roughly) except for hotfixes.
- **RAPIDS Nightly** - Updated every night and tested against some scripts to ensure stability, but should be considered unstable, although it is the latest and greatest.

.. raw:: html

    <div class="col-lg-12 col-md-12 col-sm-12 col-xs-12 d-flex text-center image">
        <div class="shadow image text-center ">
            <img src="../_static/images/free_gpu_option.png" alt="create_cluster" width=600/>
        </div>
    </div>

|

.. warning::

    Environments are not customizable in the Free GPU Instance.

The preloaded Jupyter Notebooks available in the Free GPU Instance 
home directory will work on both **RAPIDS Stable** and **RAPIDS Nightly**.

Simply open any of the Jupyter Notebooks available in the 
directory *Welcome_to_BlazingSQL_Notebooks* to get started 
with GPU-accelerated Python. 

It's that easy.

.. raw:: html

    <div class="col-lg-12 col-md-12 col-sm-12 col-xs-12 d-flex text-center image">
        <div class="shadow image text-center ">
            <img src="../_static/images/free_gpu_welcome.png" alt="create_cluster" width=600/>
        </div>
    </div>

|

If you need more processing power you can always :doc:`create private cluster <../private_clusters/cluster/index>`.

.. toctree::
    :maxdepth: 2