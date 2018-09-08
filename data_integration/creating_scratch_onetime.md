# Creating an one-time synchronization workflow

How to create an one-time data integration task from scratch.

## Before you begin

You must have created the target Hive table to synchronize the data to. For more information, see [Creating a Hive table](../data_explorer/creating_hivetable).

## Step 1: Create an data integration workflow

1. Click **Data Integration** from the left navigation tree and click **New Data Integration Workflow**.
2. In the **New Data Integration Workflow** window, provide the basic settings about the workflow.
   - Mode: Select **Create** to create a workflow from scratch. If you select **Import from Configuration**, go to [Creating by importing an existing workflow configuration](importing_existing_config).
   - Name: Enter the name of workflow.
   - Type: Select **One-time**.
   - Description: Provide a descriptive information about the workflow.
   - Select Directory: Select the directy to save the workflow.

3. Click **OK**.

## Step 2: Select the data source

When you select to synchronize from a SQL, MySQL, or Oracle database, provide the following settings:

1. Select from the list of existing data source or create a new data source. For more information, see [Data source overview](../data_source/datasource_overview).
2. Select which table to synchronize from the database.
3. (Optional) If you want to filter the data to be synchronized, provide the SQL query script.
4. (Optional) Click **Preview Data**. You can then preview the resultant data to synchronize as shown in the following figure:
    ![Preview data](di_source.png)

5. Click **Next**.


When you select to synchronize from an FTP, SFTP, or S3 data source, EnOS transforms the text-based data into a two-dimension table according to your settings:

1. Select from the list of existing data source or create a new data source. For more information, see [Data source overview](../data_source/datasource_overview).
2. Specify the URL to the data source. When the directory contains multiple files, the data records are merged. In this case, ensure that all data in the same directory has the same columns.
3. Specify the column delimiter that is used in the text-based data file, such as tabulator, comma, semicolon, space or other delimiters.
4. Specify the encoding format of the data file: UTF-8, GBK, or GB2312.
5. Specify the compression format of the data file.
6. Specify the number of header rows in the data file are to be ignored when loading the data.
7. Specify the header to add for the source table.
8. (Optional) Click **Preview Data**.
9. Click **Next**.


## Step 3: Select the target table

The only type supported now is Hive. Provide the following settings abut the target table.
1. Select the target table.
2. If the Hive table is partitioned, the partitions are automatically loaded.
3. Specify the target partition. You can specify the partition through the following methods:
   - Column name: The system creates a new partition based on the column name. If the column is date for example, and the column values are 20180501 and 20180502, then two partitions are created, each for one day.
   - Fixed value: If 2017-10-11 is entered for example, the data will be automatically synchronized to the partition 2017-10-11 in the target table.
   - Placeholder: You can use system reserved or custom parameters, from example `${cal_dt}`.
    ![Preview data](di_target.png)  

4. Specify whether to overwrite the existing data in the target table, or append the data behind the existing data records.
5. Click **Next**.

## Step 4: Configure field mapping between source and target
In this step, you'll map the source fields to the target fields.

1. For each field in the **Target Fields** column, click the source field from the **Source Fields** column to map the source with target.
   ![Mapping fields](field_mapping.png)
2. When you finish mapping each field, click **Next**.

## Step 5: Specify scheduling settings

1. Click **Scheduling Settings** from the right edge of the configuration panel.
2. Provide the basic settings:
   - Select the workflow owner from the list of users in the organization who have access to data integration.
   - (Optional) Provide a description.
   - Select how to alert the workflow owner.

## Step 6: Specify parameters

When parameters are used when you configure the data source and target, specify parameter values.

## Step 7: Configure concurrency
Select the number of concurrent connections to establish and click **Next**.

The database endures a larger load when you set a larger concurrency number. When the total transmission rate is fixed, the rate of a single concurrent connection is smaller.


## Step 8: Review and save the task configuration

Preview the settings, edit when necessary, and save the synchronization configuration.

## What to do next

After the data is synchronized from the data source, you can schedule other processing tasks against the data. For more information, see [Data IDE](../dataide/dataide_overview).

## What's next

Click **Pre-run** to manually trigger the task.
