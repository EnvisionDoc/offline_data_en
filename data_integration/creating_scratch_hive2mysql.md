# Synchronize data in EnOS Hive to target database

You can synchronize the data in EnOS Hive to the target database for data analytics and report creation purpose.

EnOS supports to synchronize Hive data to the following databases:

- External MySQL database
- EnOS report DB

## Before you begin

You must have created the target table before synchronizing:

- If you synchronize the data to the external MySQL database, you must establish and verify the connection in **Data Source** and create a target table. For more information, see [Configuring an SQL or MySQL Server data source](https://docs.envisioniot.com/docs/offline-data/en/latest/data_source/connecting_mysql.html)

- If you synchronize the data to EnOS report DB, you must create a MySQL note in **Data Explorer** and create a target table. For more information, see [Getting started with Data Explorer](https://docs.envisioniot.com/docs/analysis-report/en/latest/data_explorer/gettingstarted.html).


## Step 1: Create data integration workflow

1. Click **Data Integration** from the left navigation tree and click **+** to create a data integration workflow.

2. In the **New Data Integration Workflow** window, provide the basic settings about the workflow.
   - Mode: Select **Create** to create a workflow from scratch. If you select **Import from Configuration**, go to [Creating by importing an existing workflow configuration](importing_existing_config).
   - Name: Enter the name of workflow.
   - Type: Select **One-time**.
   - Description: Provide a descriptive information about the workflow.
   - Select Directory: Select the directory to save the workflow.

3. Click **OK**.

## Step 2: Select Hive data source

To select and synchronize the data source to MySQL or EnOS report DB, follow the steps below:  

1. In **Data Source Type**, select Hive.
2. In **Source Table**, select the data table to be synchronized.
3. (Optional) In **Partition**, specify the partition to be synchronized. If not specified, all data is synchronized to the target data table.

    You can set the value of the partition by specifying:
   - Fixed value. For example, if you set the fixed value to `20180101`, data that contains `20180101` is automatically synchronized to target table.
   - Placeholder. You can specify the system scheduling parameters, such as `${cal_dt}`, or customized parameters. For more information, see [Supported system variables](../data_ide/system_variables)

5. (Optional) Click **Preview Data**. System displays 5 random data entries by default.
6. Click **Next** to select the target table.




## Step 3: Select target table

You can synchronize the Hive data either to an external MySQL database or EnOS report DB.

- To synchronize the data to an external MySQL database, follow the steps below:

  1. In **Target Source Type**, select MySQL.
  2. In **Data Sources**, select target database that the data synchronized to.
  3. In **Table Name**, select the target table that the data synchronized to.
  4. In **Data Insertion Rule**, select **Overwrite existing records** or **Insert after existing records** according to your requirement.
  5. Click **Next**.


- To synchronize the data to EnOS report DB, follow the steps below:

  1. In **Target Source Type**, select REPORTDB.
  2. In **Data Sources**, select the target table that the data synchronized to.
  3. In **Data Insertion Rule**, select **Overwrite existing records** or **Insert after existing records** according to your requirement.
  4. Click **Next**.



## What to do next

For more information about workflow scheduling settings, parameter settings, field mapping configuration, and channel control, see:

- Periodic workflow: see [Creating a periodic workflow from scratch](creating_scratch_periodic).
- Manual workflow: see [Creating a manual workflow from scratch](creating_scratch_onetime).
