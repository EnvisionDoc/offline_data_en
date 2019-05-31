# Synchronizing Data From EnOS Hive to Target Datastore

You can synchronize the data in EnOS Hive to the target database for data analytics and report creation purpose.

EnOS supports to synchronize Hive data to the following databases:

- External MySQL database
- EnOS Report DB

## Before You Begin

You must have created the target table before synchronizing:

- If you synchronize data to an external MySQL database, you must establish and verify the connection in **Data Connection** and create a target table. For more information, see [Configuring an SQL or MySQL Server Data Connection](../data_source/connecting_mysql)

- If you synchronize data to EnOS Report DB, you must create a MySQL note in **Data Explorer** and create a target table. For more information, see [Getting Started with Data Explorer](../data_explorer/gettingstarted).


## Step 1: Create a data integration task

1. Click **Data Integration** from the left navigation tree and click **+** to create a data integration task.

2. In the **New Data Integration Task** window, complete the basic settings for the task.
   - Mode: Select **Create** to create a task from scratch. If you select **Import task config**, go to [Creating Workflow by Importing Existing Configuration](importing_existing_config).
   - Name: Enter the name of the data integration task.
   - Synchronization Type: Select **Data synchronization**.
   - Scheduling Type: Select **Manual scheduling**.
   - Description: Provide descriptive information about the data integration task.
   - Select Directory: Select the directory to save the task.

3. Click **OK** to create the data integration task.


## Step 2: Select Hive data connection

To select and synchronize the data connection to external MySQL database or EnOS Report DB, take the following steps:

1. In **Data source type**, select Hive.

2. In **Source Table**, select the data table to be synchronized.

3. (Optional) In **Partition**, specify the partition to be synchronized. If not specified, all data is synchronized to the target data table.

   You can set the value of the partition by specifying:
   - Fixed value. For example, if you set the fixed value to `20180101`, data that contains `20180101` is automatically synchronized to target table.
   - Placeholder. You can specify the system scheduling parameters, such as `${cal_dt}`, or customized parameters. For more information, see [Supported System Variables](../system_variables)

4. (Optional) Click **Data Preview**. System displays 5 random data entries by default.

5. Click **Next** to select the target table.


## Step 3: Select target table

You can synchronize the Hive data either to an external MySQL database or EnOS Report DB.

- To synchronize the data to an external MySQL database, follow the steps below:

  1. In **Target source type**, select MySQL.

  2. In **Data Sources**, select target database that the data synchronized to.

  3. In **Table Name**, select the target table that the data synchronized to.

  4. In **Data Insertion Rule**, select **Insert overwrite** or **Insert into** according to your requirements.

  5. Click **Next**.


- To synchronize the data to EnOS Report DB, follow the steps below:

  1. In **Target source type**, select REPORTDB.

  2. In **Table Name**, select the target table that the data synchronized to.

  3. In **Data Insertion Rule**, select **Insert overwrite** or **Insert into** according to your requirements.

  4. Click **Next**.

## What to Do Next

For more information about task scheduling settings, parameter settings, field mapping configuration, and channel control, see:

- Periodic task: see [Synchronizing Data from External Data Connections to Hive (Periodic Scheduling)](creating_scratch_periodic).
- Manual task: see [Synchronizing Data from External Data Connection to Hive (Manual Scheduling)](creating_scratch_onetime).
