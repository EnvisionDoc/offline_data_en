Data Integration
-------------------------------

The data integration function supports synchronizing data between extensive heterogeneous data sources.

The major use cases of data integration are to help data developers synchronize structured data from external source databases to the Hive Library in EnOS and from the EnOS Hive database to external target databases.

A data integration workflow is specific type of workflow. The essence of a data integration workflow is a workflow with a single data-integration type of task.

The data integration function only supports synchronization of structured data, that is data which can be abstracted as two-dimensional tables.

Unstructured data such as MP3 is not supported by data integration. However, you can schedule SHELL-type of tasks in a workflow to synchronize the unstructured data. For information about unstructured data synchronization, `Data IDE <../data_ide/index>`__


.. toctree::
   :maxdepth: 1
   :caption: Learn

   scenarios

.. toctree::
   :maxdepth: 1
   :caption: How-to's

   creating_scratch_onetime
   creating_scratch_periodic
   creating_scratch_hive2mysql
   importing_existing_config
   setting_parameters

.. toctree::
   :maxdepth: 1
   :caption: Reference

   ../data_ide/system_variables
