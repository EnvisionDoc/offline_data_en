# Getting Started: Creating a Customized Report

This topic describes how to synchronize data from data connection to the Report DB, and then quickly create a data visualization report online.

The following chart shows the  work flow of creating a report.

.. image:: media/workflow.png

The procedure of creating a report with EnOS Data Report service is as follows:

1. Synchronize data from data connection to the Report DB.

2. Create datasets using the synchronized data.

3. Create a report based on the datasets.

## Synchronizing Data

You can synchronize the off-line data stored in your business system to the data warehouse of the platform and process the data. After that, synchronize the data from the data warehouse to the Report DB of Data Report service to complete data preparation. Take the following steps to complete data synchronization.

1. Add data connection.

   Log in the EnOS Console and select **Data Connection** from the left navigation panel. Click the **Add Data Connection** button to complete adding Data Connections. For information about supported Data Connection types and how to configure Data Connection connection, see [Data Connection](../data_source/index.html).

2. Create target tables.

   Select **Data Explorer** from the left navigation panel and click the **New note** button to create target tables. For details, see [Creating a Hive Table](../data_explorer/creating_hivetable). If target tables already exist, you can skip this step.

3. Create data integration tasks.

   Select **Data Integration** from the left navigation panel and click **New data integration task** and complete the configuration of the task flow. Based on your business needs, you can use data filters to synchronize partial data from the data connection. For details, see [Data Integration](../data_integration/index).

4. (Optional) Create data development tasks.

   If the data ETL development logic is complex, you can create data development tasks through **Data IDE** > **Data Development** > **New Workflow**. For details about workflow configuration, see [Data IDE](../data_ide/index).

5. Run and monitor the tasks.

   After the data development task is created, click the **Pre-run** button and specify the triggering time for the task. Then, select **Workflow Operation** from the left navigation to view the running status of the workflow. For details, see [Workflow Operation](../task_monitor/index).

6. Check data synchronization results.

   After the tasks are running successfully, select **Data Explorer** from the left navigation panel to check the data that are synchronized to the Hive tables.

7. Create target tables in the Report DB.

   Select **Data Explorer** from the left navigation panel and create a note of "mysql_report" type for target tables in the Report DB. If target tables already exist, you can skip this step.

8. Synchronize table data to the Report DB.

   Select **Data Integration** from the left navigation panel and click **New data integration task** and complete the configuration of the task flow. Select **HIVE** as the data connection type and **REPORTDB** as the target source type. Click the **Pre-run** button to test the task flow, then check the task running status in **Workflow Operation**.


## Creating Datasets

After data are synchronized successfully, take the following steps to create datasets.

1. Select **Data Report > Data** from the left navigation and choose the **Data Sources** tab. Click **Switch to table** or **Switch to SQL** in the upper right corner of the page to choose the method of creating datasets.

2. Choose the **Datasets** tab and click the **Edit** button of a dataset to update the dimensions and measures. The data preparation work is completed.

For details about creating datasets, see [Creating Datasets](creating_dataset).

## Creating a Report

Data Report service provides a rich set of charts, including bar charts, line charts, pie charts, cross tables, scatter charts, indicating blocks, gauges, and highlight tables, which can satisfy various data visualization requirements.

Take the following steps to create a customized report.

1. Select **Data Report** > **Report** from the left navigation panel and click the **New Report** button.

2. On the report editing page, select a chart to be used from the **Charts** tab by double-clicking the chart icon.

3. Under the **Data** tab, select a dataset and the corresponding values for the dimension and measure.

4. Under the **Style** tab, configure the layout and display of the table.

5. (Optional) Under the **Advanced** tab, configure multi-chart association (if application). For details, see [Creating Reports](creating_report).

.. image:: media/sample.png


<!--end-->
