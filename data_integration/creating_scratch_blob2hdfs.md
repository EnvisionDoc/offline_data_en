# Synchronizing Files from External Databases to HDFS

You can synchronize files from external database to EnOS file storage system HDFS.

EnOS supports synchronizing file from the following external database:

- Azure Blob


## Before You Begin

You must have created data connection for the external database, and the external database has the files to be synchronized. For more information, see [Data Connection](/docs/offline-data/en/latest/data_source/datasource_overview.html).


## Step 1: Create a data integration task

1. Click **Data Integration** from the left navigation tree and click **+** to create a data integration task.
2. In the **New Data Integration Task** window, complete the basic settings for the task.
   - Mode: Select **Create** to create a task from scratch. If you select **Import task config**, go to [Creating Workflow by Importing Existing Configuration](importing_existing_config).
   - Name: Enter the name of the data integration task.
   - Synchronization Type: Select **File synchronization**.
   - Scheduling Type: Select **Manual scheduling**.
   - Description: Provide descriptive information about the data integration task.
   - Select Directory: Select the directory to save the task.
3. Click **OK** to create the data integration task.


## Step 2: Select data source

Select the data source of the files to be synchronized to HDFS by the following steps:

1. In **Data Source Type**, select the data source of the files to be synchronized. Currently, only Azure BLOB is supported.
2. In **Data Sources**, select the data source connection that is configured in Data Connection.
3. In **Directory or File Name**, enter the directory or file to be synchronized. Directory and file name support wild cards, system variables, and customized variables. A directory must end with "/".
4. Click **Next** to select the target.


## Step 3: Select target

Currently, the target can only be file storage system HDFS. Complete the following settings for the target:

1. In **Data Source Type**, select HDFS.
2. In **Path**, enter the sub directory to store the synchronized files, which must end with "/". If you do not specify the sub directory, the synchronized files will be stored in the root directory by default.
3. Select the **File Writing Rule**:
   - Overwrite file with the same name: If a file being synchronized has the same name with a file in the target path, the file in the target path will be overwritten.
   - Do not overwrite file with the same name: If a file being synchronized has the same name with a file in the target path, the synchronization task will be stopped immediately. The file in the target path will not be overwritten. Files that have been synchronized will be stored.
4. Click **Next**.

## Step 4: Configure concurrency

Select the number of concurrent connections to establish and click **Next**.

The database endures a larger load when you set a larger concurrency number. When the total transmission rate is fixed, the rate of a single concurrent connection is smaller.

## Step 5: Review and save the configuration

Preview the settings of the data integration task, and click **Edit** to make changes when necessary. Click **Done** to save the configuration. See the following example:

.. image:: media/sync_file.png


## What to Do Next

Click **Pre-run** and select a triggering time to test running the data integration task.

An instance will be generated after the data integration task is running. You can then trace the details about the instance through Workflow Operation. For more information, see [Workflow Operation](../task_monitor/monitoring_workflow_manual).

After files are synchronized from the source databases, you can schedule other processing tasks against the data or files. For more information, see [Data IDE](/docs/offline-data/en/latest/data_ide/index.html).
