# Data Integration Overview

The data integration function supports synchronizing data between extensive heterogeneous data connections, helping data developers with the following tasks:

- Synchronizing data: Synchronizing structured data from external source databases to the Hive Library in EnOS and from the EnOS Hive database to external target databases.
- Synchronizing files: Synchronizing files from external source databases to EnOS HDFS file storage (currently supporting Azure Blob data source).

.. image:: ../media/di_flow.png
   :alt: Figure: Data integration flow

A data integration workflow is a specific type of workflow. The essence of a data integration workflow is a workflow with a single data-integration type of task.

## Usage Scenarios

The typical scenarios of data integration are as follows.

### Full-load Data Synchronization

Synchronization of full-load of data usually happens at the initial stage of data integration. In this scenario, you synchronize full-load of data from the data connection at one-time. To achieve this scenario, see [Synchronizing Data from External Data Connection to Hive (Manaual Scheduling)](creating_scratch_onetime).

### Incremental Data Synchronization

Synchronization of incremental data usually happens after the initial stage, when you only want to synchronize the new or updated data periodically. In this scenario, you usually select the incremental data to synchronize through a `where` clause when you configure the synchronization workflow. To achieve this scenario, see [Synchronizing Data from External Data Connections to Hive (Periodic Scheduling)](creating_scratch_periodic).

### Synchronizing Files from External Databases to HDFS

Synchronization of files from external databases to HDFS. To achieve this scenario, see [Synchronizing Files from External Databases to HDFS](creating_scratch_blob2hdfs).