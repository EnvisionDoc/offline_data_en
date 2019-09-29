# Data Report Overview

EnOS Data Report is a lightweight and intelligent product for business data analysis and visualization. Primarily intended for data analysts and developers, Data Report service provides full lifecycle functions from data source connection, dataset generation, to data visualization.

Data Report can be inserted to your operation system or can exist as independent portals. You can quickly build data analysis reports through interactive drag-and-drop operation. Its reporting platform helps lower the cost and threshold to acquire, process, and analyze data, and thereby avoid duplicate efforts in front-end development.

Data Report service brings the following benefits:

- **Realtime and Efficiency**: Seamlessly integrates EnOS cloud DBs to provide a report DB with high real-time query efficiency, which greatly improves data analysis efficiency.
- **Rich Components**: Seamlessly interfaces with EnOS energy component libraries to provide a rich set of data visualization charts and controls, which meet the visualization requirements of different business scenarios.
- **Easy to use**: By creating datasets, makes data acquisition and usage easier, and reduces the complexity of data preparation.
- **Security**: Provides control over data security on the basis of the sound security system of the platform.

The major workflow for creating reports with EnOS Data Report service is as follows:
1. Connecting to _data sources_
2. Creating _datasets_
3. Making _reports_

The following figure shows sample reports that can be created with the Data Report service. For steps on creating a report, see [Getting Started](gettingstarted_report).

.. image:: media/sample.png

## Key Concepts

The key objects in a reporting platform include data sources, datasets, and reports, as described below.

.. image:: media/report_concepts.png

### Data Source

Before making a report, you need to prepare the data or specify the data source where raw data is located. By default, EnOS system creates a Report DB for organizations with the Data Report module enabled. You can use the data integration function to synchronize data from Hive to the Report DB.

### Dataset

Once a data source is connected, simple logical processing based on one or more data source tables can be performed to get a logic table that has a connection to the source tables. The logical table is a dataset. The dataset can be referenced directly in the report design phase. Therefore, you can focus on the report design instead of caring about the underlying logical processing of the source tables.

### Report

Your report contents can be customized in a WYSIWYG way by dragging the chart to adjust the layout according to your business needs. A report may contain a variety of analysis charts and controls. Filtering, multi-chart association, and other advanced operations are also supported.

## System Architecture

The architecture of the Data Report service is shown as follows.

.. image:: media/infrastructure.png

The major modules and their functions are described in the following sections.

### Data Processing Module

- **Data Source**

  By default, EnOS system creates a Report DB for organizations with the Data Report module enabled. The feature of the Report DB is high real-time query efficiency, which meets the requirement of data analysis well. You can use the data integration function to synchronize data from Hive to the Report DB, thus completing data preparation.

- **Dataset Designer**

  Dataset Designer supports flexible dataset editing functions, such as creating, editing, copying, deleting, and transforming dimensions and measures. Meanwhile, the default aggregation of dimensions and measures can also be configured, including sum, count, max, min, and avg. The dataset can be referenced directly in the report design phase, so that you can focus on the report design instead of caring about the underlying logical processing of the source tables.

- **Dataset Manager**

  Dataset Manager supports the lifecycle management of datasets, including operations like creating, deleting, copying, and editing. After connecting to data sources, datasets can be created on the basis of one or more data source tables by creating single tables or multiple tables with SQL statements.

### Data Visulization Module

- **Report Designer**

  Report Designer applies flexible tiles layout to display the interaction of report data. Report content can be customized in a WYSIWYG way by dragging the charts to adjust the layout according to business needs, supporting various methods of data filtering and query, and also providing a rich set of charts and controls for data visualization. The reports can also be exported as PDF files.

- **Report Manager**

  Report Manager supports the lifecycle management of reports, including operations like creating, deleting, copying, and editing. Furthermore, created reports can be published, either open to all people in the organization, or visible only to the report owner.

- **Visulization Control Library**

  Data Report provides a rich set of charts and controls to meet the needs of data visualization and analysis in most business scenarios. Charts include bar charts, polyline charts, pie charts, crosstabs, scatter charts, indicator blocks, dashboards, and highlight tables. Controls include query, IFrame, text box, pictures, and so on.

### Security Management Module

- **Data Security**

  By default, EnOS platform creates a Report DB for organizations with the Data Report module enabled, which isolates the storage of organization resources. Besides, the Data Report service is integrated with the EnOS IAM (indentity and access management) system. Access to published reports requires user account login and authentication.

<!--end-->