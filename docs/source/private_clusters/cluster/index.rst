.. _cluster:

=======
Cluster
=======

If your application/data requires more compute power than can fit on a single GPU,
BlazingSQL Notebooks provide private clusters: a managed resource and software environments with 
everything neccesary to have RAPIDS and BlazingSQL on the cloud. Using Blazing Notebooks is the easiest way to get 
started developing on GPUs!

Create a cluster
================

To get started with private clusters you will need credits in your account; check 
:doc:`Billing <../../billing/index>` section to learn how.

Creating clusters on BlazingSQL Notebooks requires only 3 parameters to start with:

- **Cluster name:** A recognizable name for your cluster.
- **Size:** Select the number of GPUs from dropdown. See :ref:`Supported cluster sizes and GPUs <cluster_sizes>` section below.
- **Auto Suspend:** Time the cluster will shutdown if not being used. 

.. raw:: html

    <div class="col-lg-12 col-md-12 col-sm-12 col-xs-12 d-flex text-center image">
        <div class="shadow image text-center ">
            <img src="../../_static/images/create_cluster_requiered.png" alt="create_cluster" width=400/>
        </div>
    </div>

|

Some default values are preset but you can adjust them if you click on 
the **Advanced options**.

.. raw:: html

    <div class="col-lg-12 col-md-12 col-sm-12 col-xs-12 d-flex text-center image">
        <div class="shadow image text-center ">
            <img src="../../_static/images/advanced_options.png" alt="create_cluster" width=400/>
        </div>
    </div>

|

Available options:

- **Region:** defults to *us-east-1*. Available regions are *us-east-1*, *us-east-2*, *us-west-1*, *us-west-1*.
- **Environment:** defaults to *"rapids-stable"*. Built-in environments are *rapids-stable* and *rapids-nightly*. To learn how to create environments refer to the :doc:`Environments <../environments/index>` part.

.. _cluster_sizes:

Supported cluster sizes and GPUs
================================

To provide flexibility and help with handling any type of workload
we support clusters that can be comprised of 1 to 64 GPUs. 
The table below shows the available SKUs with their capabilities and price.

.. list-table:: List of available cluster sizes
   :widths: 25 25 50 25
   :header-rows: 1

   * - SKU
     - Number of GPUs
     - GPU RAM
     - Credits per hour
   * - **X-Small**
     - 1
     - 16GB
     - 1 credit
   * - **Small**
     - 2
     - 32GB
     - 2 credits
   * - **Medium**
     - 4
     - 64GB
     - 4 credits
   * - **Large**
     - 8
     - 128GB
     - 8 credits
   * - **X-Large**
     - 16
     - 256GB
     - 16 credits
   * - **2X-Large**
     - 32
     - 512GB
     - 32 credits
   * - **3X-Large**
     - 64
     - 1024GB
     - 64 credits

Blazing Notebooks runs on NVIDIA T4 GPUs, each with 16GB of RAM.

Start cluster
=============

If you create a new cluster, once it is deployed it will be returned to 
you in a running state. 

After you shut down the cluster, either manually or the auto-suspend did that for you
(see :ref:`Manual and auto-suspend <manual_auto_suspend>`), you can start a cluster
in two ways:

1. In the *tiles* view click on **Actions** and select **Start**

.. raw:: html

    <div class="col-lg-12 col-md-12 col-sm-12 col-xs-12 d-flex text-center image">
        <div class="shadow image text-center ">
            <img src="../../_static/images/cluster_start_tiles.png" alt="create_cluster" width=300/>
        </div>
    </div>

|

2. In the *list* view click on the **Play** button.

.. raw:: html

    <div class="col-lg-12 col-md-12 col-sm-12 col-xs-12 d-flex text-center image">
        <div class="shadow image text-center ">
            <img src="../../_static/images/cluster_start_list.png" alt="create_cluster" width=500/>
        </div>
    </div>


Delete cluster
==============

If you want to delete cluster, there are two ways to achieve that.

1. In the *tiles* view click on **Actions** and select **Delete**.

.. raw:: html

    <div class="col-lg-12 col-md-12 col-sm-12 col-xs-12 d-flex text-center image">
        <div class="shadow image text-center ">
            <img src="../../_static/images/cluster_delete_tiles.png" alt="create_cluster" width=300/>
        </div>
    </div>

|

2. In the *list* view click on the **Delete** button.

.. raw:: html

    <div class="col-lg-12 col-md-12 col-sm-12 col-xs-12 d-flex text-center image">
        <div class="shadow image text-center ">
            <img src="../../_static/images/cluster_delete_list.png" alt="create_cluster" width=500/>
        </div>
    </div>

|

To finalize the deletion of a cluster you need to confirm that in the pop-up window.

.. raw:: html

    <div class="col-lg-12 col-md-12 col-sm-12 col-xs-12 d-flex text-center image">
        <div class="shadow image text-center ">
            <img src="../../_static/images/delete_cluster_confirmation.png" alt="create_cluster" width=300/>
        </div>
    </div>

.. _manual_auto_suspend:

Manual and auto-suspend
=======================
You can stop your cluster manually (see :ref:`below <manual_stop>`). However, if 
by any chance you forget, the :ref:`auto-suspend <auto_stop>` process will turn off your cluster 
automatically after the predefined period of time.

.. _manual_stop:

Manual suspend
---------------

To stop you cluster manually you have two ways:

1. In the *tiles* view click on **Actions** and select **Stop**.

.. raw:: html

    <div class="col-lg-12 col-md-12 col-sm-12 col-xs-12 d-flex text-center image">
        <div class="shadow image text-center ">
            <img src="../../_static/images/manual_suspend.png" alt="manual_suspend" width=300/>
        </div>
    </div>

|

2. In the *list* view click on the **Stop** button.

.. raw:: html

    <div class="col-lg-12 col-md-12 col-sm-12 col-xs-12 d-flex text-center image">  
        <div class="shadow image text-center ">
            <img src="../../_static/images/suspend_cluster_list.png" alt="suspend_cluster_list" width=500/>
        </div>
    </div>

|

Either way you choose, once you click the *"Stop"* button the cluster status will change automatically from *"Running"* to *"Stopping Cluster (Manual)"*.

.. raw:: html

    <div class="col-lg-12 col-md-12 col-sm-12 col-xs-12 d-flex text-center image">  
        <div class="shadow image text-center ">
            <img src="../../_static/images/manualsuspend.png" alt="create_cluster" width=300/>
        </div>
    </div>

|

After the proccess finishes the status of the cluster will be *"Stopped"*.

.. raw:: html

    <div class="col-lg-12 col-md-12 col-sm-12 col-xs-12 d-flex text-center image">  
        <div class="shadow image text-center ">
            <img src="../../_static/images/stopped_clusters.png" alt="create_cluster" width=600/>
        </div>
    </div>

.. _auto_stop:

Auto-suspend
-------------

The auto-suspend process will shut down your cluster after the predefined time of inactivity specified during the cluster creation. 

.. raw:: html

    <div class="col-lg-12 col-md-12 col-sm-12 col-xs-12 d-flex text-center image">  
        <div class="shadow image text-center ">
            <img src="../../_static/images/autosuspend.png" alt="create_cluster" width=300/>
        </div>
    </div>

|

Once the cluster starts shutting down, the status will change from *"Running"* to *"Stopping Cluster (Auto)"*.

.. raw:: html

    <div class="col-lg-12 col-md-12 col-sm-12 col-xs-12 d-flex text-center image">  
        <div class="shadow image text-center ">
            <img src="../../_static/images/auto_suspend.png" alt="create_cluster" width=300/>
        </div>
    </div>

|

Once the proccess finishes the status of the cluster will be *"Stopped"*.

.. raw:: html

    <div class="col-lg-12 col-md-12 col-sm-12 col-xs-12 d-flex text-center image">  
        <div class="shadow image text-center ">
            <img src="../../_static/images/stopped_clusters.png" alt="create_cluster" width=600/>
        </div>
    </div>

Launching Jupyter Lab
=====================

To launch the :doc:`workspace / Jupyter Lab <../workspace/index>` click the **Launch** button.

.. raw:: html

    <div class="col-lg-12 col-md-12 col-sm-12 col-xs-12 d-flex text-center image">  
        <div class="shadow image text-center ">
            <img src="../../_static/images/launch_cluster.png" alt="launch_cluster" width=300/>
        </div>
    </div>

Then you will be redirected to Jupyter Lab window. 
All the dependencies that are necessary to work with BlazingSQL and RAPIDS are already here (see :doc:`Environments <../environments/index>` part for more details). 

.. 
    _Also you can install all the packages and extensions that you want.

.. raw:: html

    <img src="../../_static/images/jupyter_window.png" alt="jupyter_window" width=700/>

.. toctree::
    :maxdepth: 2