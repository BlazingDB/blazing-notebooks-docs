.. _cluster:

=======
Cluster
=======

BlazingSQL Notebooks app provide private cluster's and manages resources, software environments, 
and everything neccesary to have RAPIDS and BlazingSQL on the cloud.

In the next sections we will learn more about how to create, launch, 
delete and suspend private Dask clusters.

Create a cluster
================

Creating clusters on BlazingSQL Notebooks is easy only setting values for some parameters.

**Required parameters:**

**Cluster name:** Should be something that is easy for you to identify your cluster.

**Size:** This parameter is about the number of GPUs in your cluster. There is options to select from 1 to 
64 GPUs.

**Auto Suspend:** It is about in what time your cluster should start the autosuspend cluster after finish the last execution process. 

.. raw:: html

    <img src="../../_static/images/create_cluster_requiered.png" alt="create_cluster" width=600/>
    
**Default values:**

**Region:** The default value will be us-east-1

**Environment:** By default it will be *"rapids-stable"*

Those parameteres could be changed and we will explain more about that in Advanced options section.


Supported cluster sizes and GPUs
================================

For private cluster BlazingSQL Notebooks app support clusters that contain from 1 to 64 GPUs. The cost of each type of cluster is 1 USD per GPU as we can see in the image.

.. raw:: html

    <img src="../../_static/images/size_cluster.png" alt="create_cluster"/>

Advanced options
================

Creating private cluster allow users to configure two advanced options:

**Region:** We can selected some specific region. The options for that parameter are us-east-1, us-east-2, us-west-1, us-west-1

**Environment:** If you are a new user, you have two created environments. But you also can create custom environments.

.. raw:: html

    <img src="../../_static/images/advanced_options.png" alt="create_cluster"/>


Delete cluster
==============

To delete cluster, there are two ways to do it.

In menu *"Cluster"*:

.. raw:: html

    <img src="../../_static/images/delete_cluster_grid.png" alt="create_cluster"/>

In *"List clusters"*:

.. raw:: html

    <img src="../../_static/images/delete_cluster_list.png" alt="create_cluster"/>

   
You can also have to click on delete button in one of the options and you will see this window.

.. raw:: html

    <img src="../../_static/images/delete_cluster_confirmation.png" alt="create_cluster"/>


Finally, you have to do click on *"Delete"* button

Manual and auto-suspend
=======================

Manual suspend:
---------------

You have two ways to suspend cluster manually. One of them is from the cluster box. 

.. raw:: html

    <img src="../../_static/images/manual_suspend.png" alt="manual_suspend"/>

The second one is from list clusters.

.. raw:: html

    <img src="../../_static/images/suspend_cluster_list.png" alt="suspend_cluster_list"/>

For both cases, after you do click on *"Stop"* button you will see that the cluster status change automatically from *"Running"* to *"Stopping Cluster (Manual)"*.

.. raw:: html

    <img src="../../_static/images/manualsuspend.png" alt="create_cluster"/>

Auto-suspend:
-------------

The auto-suspend process start according to the time that you especify when you create the cluster. 

.. raw:: html

    <img src="../../_static/images/autosuspend.png" alt="create_cluster"/>

When you stop to use the cluster, after the auto-suspend time, the cluster will change the status from *"Running"* to *"Stopping Cluster (Auto)"*

.. raw:: html

    <img src="../../_static/images/auto_suspend.png" alt="create_cluster"/>

In each case, for manual and auto-suspend, after the proccess finish the status of the cluster will be *"Stopped"*.

.. raw:: html

    <img src="../../_static/images/stopped_clusters.png" alt="create_cluster"/>

Jupyter Lab
===========

In clusterbox we have the "Launch" button. You only have to do click there

.. raw:: html

    <img src="../../_static/images/launch_cluster.png" alt="launch_cluster"/>

Then you will be redirected to Jupyter lab window. Here you will have all the dependencies what are necessary to work with blazingSQL and RAPIDS. Also you can install all the packages and extensions that you want.

.. raw:: html

    <img src="../../_static/images/jupyter_window.png" alt="jupyter_window"/>

.. toctree::
    :maxdepth: 2