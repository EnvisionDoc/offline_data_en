# Common library

EnOS provides various built-in SDKs in its common library to help you access and process data more conveniently. These SDKs lower the development thresholds and improve development efficiency.

## What's provided in the library


<table border="1" cellspacing="0" cellpadding="0">
  <tr>
    <td><p align="center"><strong>SDK name</strong></p ></td>
    <td><p align="center"><strong>Description</strong></p ></td>
  </tr>
  <tr>
    <td><p>SYNC_HDFS_TO_S3</p ></td>
    <td><p>Synchronize data from a specified path in HDFS to a specified   path in an S3 database.</p ></td>
  </tr>
  <tr>
    <td><p>COLUMNS_TO_ROWS</p ></td>
    <td><p>Converts row data of your HIVE table, where each row contains   values of all data collecting points of a device at a time, into a table   where each row contains historical values of a single data collecting point.</p ></td>
  </tr>
  <tr>
    <td><p>SYNC_MDM</p ></td>
    <td><p>Synchronizes master data to HDFS.</p ></td>
  </tr>
  <tr>
    <td><p>SYNC_REPORT_DB</p ></td>
    <td><p>Performs one-time synchronization of full-load of data from   Hive table to your target table.</p ></td>
  </tr>
  <tr>
    <td><p>FLATTEN_POINTS</p ></td>
    <td><p>Converts EnOS raw point data (each row contains historical   values of a single data collecting point) to sql-like row data (each row   contains values of all data collecting points of a device at a time).</p ></td>
  </tr>
  <tr>
    <td><p>POWER_DATA_INTERPOLATION</p ></td>
    <td><p>Interpolates power data, especially for the missing data of   production.</p ></td>
  </tr>
  <tr>
    <td><p>SYNC_REPORT_STRUCTURE</p ></td>
    <td><p>Transfers table structure from Hive database, to MySQL report   database.</p ></td>
  </tr>
  <tr>
    <td><p>SHORT_TERM_LOAD_FORECAST</p ></td>
    <td><p>For different power consumers in the grid, provides 0-6 days   load forecast for different-level of time granularity (15 min, 30 min, 1   hour, 1 day) based on historical data and optionally weather data.</p ></td>
  </tr>
  <tr>
    <td><p>HADOOP_FILE_CRUSHER</p ></td>
    <td><p>Combines many small files into fewer larger files.</p ></td>
  </tr>
</table>


## How to use the SDK

The major procedure of using the built-in SDK is as follows:

1. In **Data IDE** > **Task Designer**, browse the Common Library tree and locate the SDK that you want to use.
2. Double-click the version of the script and review the details about the script.
  ![Built-in script](media/scenario_built-in.png)

3. Click **Use the SDK**.

4. In the pop-out window, provide settings about the workflow.
  ![Workflow with built-in script](media/built-in_workflow.png)

5. Provide the scheduling settings. For more information, see [Creating a one-time workflow](creating_workflow_onetime) or [Creating a periodic workflow](creating_workflow_periodic).
