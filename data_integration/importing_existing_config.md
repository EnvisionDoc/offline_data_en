# Creating a Task by Importing Existing Configuration

If you have existing task configuration that you want to reuse for the new data integration task, import the configuration file.

## Before You Begin

You must have a task or workflow configuration file stored locally. For information about how to export an existing task or workflow as a configuration file, see [Exporting a Workflow](../data_ide/operating_workflow#exporting-a-workflow).

## Procedure

1. Click **Data Integration** from the left navigation tree and click **+** to create a data integration task.

2. In the **New Data Integration Task** window, complete the basic settings for the task.

   - Mode: select **Import task config**.
   - Name: Enter the name of the task.
   - Upload File: Browse and select the configuration file in your local file system.
   - Synchronization Type: Select whether synchronize data or files.
   - Scheduling Type: Select whether to create a periodic task that is run automatically based on scheduling parameters, or a one-time task that is run only when manually triggered.
   - Description: Provide descriptive information about the task.
   - Select Directory: Select the directy to save the task.

3. Click **OK**.

4. Edit the settings that are loaded from the configuration file.

   - If you selected to create a periodic task in step 2, see [Synchronizing Data from External Data Connections to Hive (Periodic Scheduling)](creating_scratch_periodic).
   - If you selected to create a one-time task in step 2, see [Synchronizing Data from External Data Connection to Hive (Manual Scheduling)](creating_scratch_onetime).

## What to Do Next

Click **Pre-run** and select a triggering time to test running the data integration task.

After a task is running, an instance will be generated. You can then trace the details about the instance through the Workflow Operation. For more information, see [Workflow Operation](../task_monitor/index).

After the data is synchronized from the data connection, you can schedule other processing tasks against the data. For more information, see [Data IDE](../data_ide/dataide_overview).
